# EXL_GetCellBorderT

## Description
Get cell top border - weight, color, is enable and style.

```pascal
FUNCTION EXL_GetCellBorderT(
				sheetIndex     : INTEGER;
				cellRow        : INTEGER;
				cellColumn     : INTEGER;
				VAR outWeight  : INTEGER;
				VAR outColor   : INTEGER;
				VAR outEnabled : BOOLEAN;
				VAR outStyle   : INTEGER): BOOLEAN;
```

```python
def vs.EXL_GetCellBorderT(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outWeight, outColor, outEnabled, outStyle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outWeight|INTEGER|   |
|outColor|INTEGER|   |
|outEnabled|BOOLEAN|   |
|outStyle|INTEGER|   |

## Examples
```pascal
resultOK := EXL_GetCellBorderT(1, 2, 3, 10, 5, TRUE, 1);
```
```python
import vs

# Get cell top border - weight, color, is enable and style.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outWeight, outColor, outEnabled, outStyle = vs.EXL_GetCellBorderT(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellBorderT returned: ' + str((ok, outWeight, outColor, outEnabled, outStyle)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
