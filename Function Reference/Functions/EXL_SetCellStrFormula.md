# EXL_SetCellStrFormula

## Description
Write cell value as a string formula.

```pascal
FUNCTION EXL_SetCellStrFormula(
				sheetIndex    : INTEGER;
				cellRow       : INTEGER;
				cellColumn    : INTEGER;
				formulaString : STRING;
				formulaValue  : STRING): BOOLEAN;
```

```python
def vs.EXL_SetCellStrFormula(sheetIndex, cellRow, cellColumn, formulaString, formulaValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|formulaString|STRING|   |
|formulaValue|STRING|   |

## Examples
```pascal
resultOK := EXL_SetCellStrFormula(1, 2, 3, 'Example', 'Example');
```
```python
import vs

# Write cell value as a string formula.
sheetIndex = 1
cellRow = 10
cellColumn = 5
formulaString = 'Example'
formulaValue = 'Example'

ok = vs.EXL_SetCellStrFormula(sheetIndex, cellRow, cellColumn, formulaString, formulaValue)
if ok:
    vs.Message('EXL_SetCellStrFormula succeeded')
else:
    vs.Message('EXL_SetCellStrFormula failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
