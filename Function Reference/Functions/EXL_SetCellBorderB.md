# EXL_SetCellBorderB

## Description
Set cell bottom border - weight, color, enable and style.

```pascal
FUNCTION EXL_SetCellBorderB(
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
def vs.EXL_SetCellBorderB(sheetIndex, cellRow, cellColumn, weight, color, style, enabled):
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
resultOK := EXL_SetCellBorderB(1, 2, 3, 10, 5, 1, TRUE, FALSE);
```
```python
import vs

# Set cell bottom border - weight, color, enable and style.
sheetIndex = 1
cellRow = 10
cellColumn = 5
weight = 1
color = 5
style = 0
enabled = True

ok, outInconsistencyFound = vs.EXL_SetCellBorderB(sheetIndex, cellRow, cellColumn, weight, color, style, enabled)
vs.Message('EXL_SetCellBorderB returned: ' + str((ok, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
