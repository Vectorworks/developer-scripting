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

## Examples
```pascal
resultOK := EXL_SetCellFont(1, 2, 3, 10, 5, 1, 2, TRUE);
```
```python
import vs

# Set cell font style, font size, font index, text color index and is
# inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5
fontStyle = 0
fontSize = 1
fontIndex = 1
textColorIndex = 1

ok, outInconsistencyFound = vs.EXL_SetCellFont(sheetIndex, cellRow, cellColumn, fontStyle, fontSize, fontIndex, textColorIndex)
vs.Message('EXL_SetCellFont returned: ' + str((ok, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
