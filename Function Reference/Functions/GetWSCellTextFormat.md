# GetWSCellTextFormat

## Description
Returns text format settings for a cell in the referenced worksheet.

* Table - Text Style

| Style | Constant |
|-------|----------|
| Plain | 0 |
| Bold | 1 |
| Italic | 2 |
| Underline | 4 |
| Outline | 8 |
| Shadowed | 16 |

```pascal
PROCEDURE GetWSCellTextFormat(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR fontIndex : INTEGER;
				VAR size      : INTEGER;
				VAR style     : INTEGER);
```

```python
def vs.GetWSCellTextFormat(worksheet, row, column):
    return (fontIndex, size, style)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|fontIndex|INTEGER|Font index of cell text.|
|size|INTEGER|Font size of cell text.|
|style|INTEGER|Font style of cell text.|

## Remarks
Note: Outline and Shadow only display on the Mac

FontStyle integer is the sum of applicable attributes.

## Examples
```pascal
2:	BEGIN
		ShowWS( WSh, TRUE );{activate and Open to Show single change}
		SetTopVisibleWS( WSh );
		{SelectSS(hWS);{activate and Open to Show single change}
		GetWSCellTextFormat( WSh, row, col, fontIdx, fontSize, fontStyle );
		ReplaceStr(str,gFindString,gReplString,gCase);
		SetWSCellFormula( WSh, row, col, row, col, gResultText );
		SetWSCellTextFormat(WSh,row,col,row,col,fontIdx,fontSize,fontStyle);
		ProcessFoundCell := TRUE;

{check if on a FarEast system; DefaultFontID returns Arial, and we don't want to set the font to Arial on a FarEast system }
If gBoldHeadersWKS then Style := 1 ELSE Style := 0;
IF GetPref(12222) THEN BEGIN
	GetWSCellTextFormat(tempHandle, 1, 1, defaultFont, defaultSize, defaultStyle);
	SetWSCellTextFormat(tempHandle,1,1,1,1,defaultFont,10,Style);
END

GetWSCellTextFormat(tempHandle, 1,1,fontIndex, fontSize, fontStyle);
SetWSCellTextFormat(tempHandle,1,1,1,1,fontIndex,10,1);
SetWSCellFormula(tempHandle,1,1,1,1,GetPlugInString(5004)); {nominal}
SetWSCellTextFormat(tempHandle,1,2,1,2,fontIndex,10,1);
SetWSCellFormula(tempHandle,1,2,1,2,GetPlugInString(5005)); {count}
```
```python
import vs

# Returns text format settings for a cell in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

fontIndex, size, style = vs.GetWSCellTextFormat(worksheet, row, column)
vs.Message('GetWSCellTextFormat returned: ' + str((fontIndex, size, style)))
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
