# EXL_SetCellBorderL

## Description
Set cell left border - weight, color, enable and style.

```pascal
FUNCTION EXL_SetCellBorderL(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				weight                    : INTEGER;
				color                     : INTEGER;
				style                     : INTEGER;
				enabled                   : BOOLEAN;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_SetCellBorderL(sheetIndex, cellRow, cellColumn, weight, color, style, enabled):
    return (BOOLEAN, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|weight|INTEGER|   |
|color|INTEGER|   |
|style|INTEGER|   |
|enabled|BOOLEAN|   |
|outInconsistencyFound|BOOLEAN|   |

## Examples
```pascal
resultOK := EXL_SetCellBorderL(1, 2, 3, 10, 5, 1, TRUE, FALSE);
```
```python
import vs

# Set cell left border - weight, color, enable and style.
sheetIndex = 1
cellRow = 10
cellColumn = 5
weight = 1
color = 5
style = 0
enabled = True

ok, outInconsistencyFound = vs.EXL_SetCellBorderL(sheetIndex, cellRow, cellColumn, weight, color, style, enabled)
vs.Message('EXL_SetCellBorderL returned: ' + str((ok, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
