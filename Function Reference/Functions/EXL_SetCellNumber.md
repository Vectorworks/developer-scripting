# EXL_SetCellNumber

## Description
Write the cell value as a number.

```pascal
FUNCTION EXL_SetCellNumber(
				sheetIndex : INTEGER;
				cellRow    : INTEGER;
				cellColumn : INTEGER;
				value      : REAL): BOOLEAN;
```

```python
def vs.EXL_SetCellNumber(sheetIndex, cellRow, cellColumn, value):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
resultOK := EXL_SetCellNumber(1, 2, 3, 1.0);
```
```python
import vs

# Write the cell value as a number.
sheetIndex = 1
cellRow = 10
cellColumn = 5
value = 1.0

ok = vs.EXL_SetCellNumber(sheetIndex, cellRow, cellColumn, value)
if ok:
    vs.Message('EXL_SetCellNumber succeeded')
else:
    vs.Message('EXL_SetCellNumber failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
