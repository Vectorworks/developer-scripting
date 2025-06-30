# GetWSCellTextFormat

## Description
Returns text format settings for a cell in the referenced worksheet.

* Table - Text Style

| Style | Constant |
|-------|----------|
| Plain | 0 |
| Bold | 1 |
| Italic | 2 |
| Underline | 4 |
| Outline | 8 |
| Shadowed | 16 |

```pascal
PROCEDURE GetWSCellTextFormat(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR fontIndex : INTEGER;
				VAR size      : INTEGER;
				VAR style     : INTEGER);
```

```python
def vs.GetWSCellTextFormat(worksheet, row, column):
    return (fontIndex, size, style)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|fontIndex|INTEGER|Font index of cell text.|
|size|INTEGER|Font size of cell text.|
|style|INTEGER|Font style of cell text.|

## Remarks
Note: Outline and Shadow only display on the Mac

FontStyle integer is the sum of applicable attributes.

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
