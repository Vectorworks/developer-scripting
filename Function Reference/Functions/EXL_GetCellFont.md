# EXL_GetCellFont

## Description
Get cell font style, font size, font index, text color index and is inconsistency found.

```pascal
FUNCTION EXL_GetCellFont(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				VAR outFontStyle          : INTEGER;
				VAR outFontSize           : INTEGER;
				VAR outFontIndex          : INTEGER;
				VAR outTextColorIndex     : INTEGER;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_GetCellFont(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outFontStyle, outFontSize, outFontIndex, outTextColorIndex, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outFontStyle|INTEGER|   |
|outFontSize|INTEGER|   |
|outFontIndex|INTEGER|   |
|outTextColorIndex|INTEGER|   |
|outInconsistencyFound|BOOLEAN|   |

## Examples
```pascal
resultOK := EXL_GetCellFont(1, 2, 3, 10, 5, 1, 2, TRUE);
```
```python
import vs

# Get cell font style, font size, font index, text color index and is
# inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outFontStyle, outFontSize, outFontIndex, outTextColorIndex, outInconsistencyFound = vs.EXL_GetCellFont(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellFont returned: ' + str((ok, outFontStyle, outFontSize, outFontIndex, outTextColorIndex, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
