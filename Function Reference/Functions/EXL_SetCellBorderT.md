# EXL_SetCellBorderT

## Description
Set cell top border - weight, color, enable and style.

```pascal
FUNCTION EXL_SetCellBorderT(
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
def vs.EXL_SetCellBorderT(sheetIndex, cellRow, cellColumn, weight, color, style, enabled):
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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
