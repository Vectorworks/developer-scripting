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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
