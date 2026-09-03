# 28. Symbol Instance Schedule

## Description
Walks the document's symbol library, and for each definition writes one row
into a worksheet: the symbol name, a live `=COUNT((S='name'))` formula that
tallies its instances, and the sum of a numeric record field (e.g. cost) if
the symbol carries one. Real precedent:
`VW_Spotlight/Includes/CableTools/Make Data WKS.px` and
`VW_Mech/Includes/PartsList.px`.

## What This Demonstrates
- Iterating symbol *definitions* with
  [`FSymDef`](../FSymDef.md) /
  [`NextSymDef`](../NextSymDef.md) — not instances
- Building live `=COUNT` and `=SUM` formulas that stay accurate as the user
  places more instances
- Escaping single quotes inside a criteria embedded in a formula

## Python Script
```python
import vs

kWSName = 'Symbol Schedule'


def cell(ws, row, col, text):
    vs.SetWSCellFormula(ws, row, col, row, col, text)


def esc(name):
    """Double single quotes for embedding a name inside a Pascal-style string."""
    return name.replace("'", "''")


def count_symbol_formula(sym_name):
    return "=COUNT((S='" + esc(sym_name) + "'))"


def sum_field_formula(sym_name, rec_name, field_name):
    """=SUM((S='sym')&(R IN ['rec']), 'rec'.'field') pattern.

    Not every symbol carries records — the formula degrades to empty for
    symbols that don't match, so it's safe to apply to every row.
    """
    return ("=SUM(('" + esc(rec_name) + "'.'" + esc(field_name) + "'),"
            "(S='" + esc(sym_name) + "') & (R IN ['" + esc(rec_name) + "']))")


def enumerate_symbol_defs():
    """Yield each top-level symbol definition handle in the document."""
    h = vs.FSymDef()
    while h is not None:
        yield h
        h = vs.NextSymDef(h)


def main():
    defs = list(enumerate_symbol_defs())
    if not defs:
        vs.AlrtDialog('Document has no symbol definitions.')
        return

    stale = vs.GetObject(kWSName)
    if stale is not None:
        vs.DelObject(stale)
    ws = vs.CreateWS(kWSName, len(defs) + 2, 3)

    cell(ws, 1, 1, 'Symbol')
    cell(ws, 1, 2, 'Instances')
    cell(ws, 1, 3, "Total Cost (Part Info.UnitCost * n)")
    vs.SetWSCellTextFormat(ws, 1, 1, 1, 3, vs.GetFontID('Arial'), 10, 1)

    for i, sd in enumerate(defs, start=2):
        name = vs.GetSDName(sd)
        cell(ws, i, 1, name)
        cell(ws, i, 2, count_symbol_formula(name))
        cell(ws, i, 3, sum_field_formula(name, 'Part Info', 'UnitCost'))

    # Grand total: sum column 2 (instance counts) from row 2 to N+1.
    last_data_row = len(defs) + 1
    total_row = len(defs) + 2
    cell(ws, total_row, 1, 'TOTAL')
    cell(ws, total_row, 2, '=SUM(B2:B' + str(last_data_row) + ')')
    cell(ws, total_row, 3, '=SUM(C2:C' + str(last_data_row) + ')')
    vs.SetWSCellTextFormat(ws, total_row, 1, total_row, 3,
                           vs.GetFontID('Arial'), 10, 1)

    vs.SetWSColumnWidth(ws, 1, 1, 220)
    vs.SetWSColumnWidth(ws, 2, 3, 130)
    vs.SetWSCellAlignment(ws, 2, 2, total_row, 3, 4)     # right-align numbers

    vs.RecalculateWS(ws)
    vs.ShowWS(ws, True)
    vs.Message(str(len(defs)), ' symbol definition(s) scheduled.')


main()
```

## Notes
- **Symbol definitions live in the symbol library, not on any layer.** They
  are enumerated via `FSymDef`/`NextSymDef` (not `FObject`).
- **`=COUNT((S='name'))` is layer-independent** — it walks the entire
  document. Add `& (L='Floor Plan')` to scope it.
- **Nested symbols:** the count only sees direct instances. To count
  through wall-inserted symbols too, add `INSYMBOL & INOBJECT` to the
  criteria: `=COUNT((INSYMBOL & INOBJECT) & (S='Chair'))`.

## Key Functions
- [`FSymDef`](../FSymDef.md), [`NextSymDef`](../NextSymDef.md), [`GetSDName`](../GetSDName.md)
- [`SetWSCellFormula`](../SetWSCellFormula.md), [`SetWSCellTextFormat`](../SetWSCellTextFormat.md), [`SetWSCellAlignment`](../SetWSCellAlignment.md)
- [`SetWSColumnWidth`](../SetWSColumnWidth.md)
