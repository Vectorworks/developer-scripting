# EXL_SetCellFont

## Description
Set cell font style, font size, font index, text color index and is inconsistency found.

```pascal
FUNCTION EXL_SetCellFont(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				fontStyle                 : INTEGER;
				fontSize                  : INTEGER;
				fontIndex                 : INTEGER;
				textColorIndex            : INTEGER;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_SetCellFont(sheetIndex, cellRow, cellColumn, fontStyle, fontSize, fontIndex, textColorIndex):
    return (BOOLEAN, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|fontStyle|INTEGER|   |
|fontSize|INTEGER|   |
|fontIndex|INTEGER|   |
|textColorIndex|INTEGER|   |
|outInconsistencyFound|BOOLEAN|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
