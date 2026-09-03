# EXL_SetCellString

## Description
Write the cell value as a string.

```pascal
FUNCTION EXL_SetCellString(
				sheetIndex : INTEGER;
				cellRow    : INTEGER;
				cellColumn : INTEGER;
				value      : STRING): BOOLEAN;
```

```python
def vs.EXL_SetCellString(sheetIndex, cellRow, cellColumn, value):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|value|STRING|   |

## Examples
```pascal
resultOK := EXL_SetCellString(1, 2, 3, 'Example');
```
```python
import vs

# Write the cell value as a string.
sheetIndex = 1
cellRow = 10
cellColumn = 5
value = 'Example'

ok = vs.EXL_SetCellString(sheetIndex, cellRow, cellColumn, value)
if ok:
    vs.Message('EXL_SetCellString succeeded')
else:
    vs.Message('EXL_SetCellString failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
