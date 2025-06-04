# EXL_GetCellBorderR

## Description
Get cell right border - weight, color, is enable and style.

```pascal
FUNCTION EXL_GetCellBorderR(
				sheetIndex     : INTEGER;
				cellRow        : INTEGER;
				cellColumn     : INTEGER;
				VAR outWeight  : INTEGER;
				VAR outColor   : INTEGER;
				VAR outEnabled : BOOLEAN;
				VAR outStyle   : INTEGER): BOOLEAN;
```

```python
def vs.EXL_GetCellBorderR(sheetIndex, cellRow, cellColumn):
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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
