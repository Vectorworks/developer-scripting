# GetTextStyle

## Description
Procedure GetTextStyle returns the text style at a specified position within the referenced text object.

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

**Table - Text Style**

| Style                | Constant |
|----------------------|----------|
| Plain                | 0        |
| Bold                 | 1        |
| Italic               | 2        |
| Underline            | 4        |
| Outline              | 8        |
| Shadowed             | 16       |
| Superscript (VW 2011+)| 32      |
| Subscript (VW 2011+) | 64       |

```pascal
FUNCTION GetTextStyle(
				TextHd   : HANDLE;
				Position : INTEGER): INTEGER;
```

```python
def vs.GetTextStyle(TextHd, Position):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Examples
```pascal
		TextOrigin(0,0);
		CreateText(Concat(' ', KNNoteNo));
		SetTextFont( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextFont( textFoundH, 0 ) );
		SetTextSize( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextSize( textFoundH, 0 ) );
		SetTextStyle( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextStyle( textFoundH, 0 ) );
		AddNumberWidth := GetTextWidth( LNewObj );
		DelObject(LNewObj);
	end ELSE AddNumberWidth := 0;
END ELSE AddNumberWidth := 0;

BEGIN
	{get the documents default text font ID and style - these will be used to format the ws cells}
	createText ('0');
	defaultFontID := GetTextFont (LNewObj, 0);
	defaultFontStyle := GetTextStyle (LNewObj, 0);
	DelObject (LnewObj);
	IF (defaultFontStyle = 0) | (defaultFontStyle = 2) | (defaultFontStyle = 4) | (defaultFontStyle = 6) THEN
		boldFontStyle := defaultFontStyle + 1
	ELSE boldFontStyle := defaultFontStyle;

TextOrigin (0, 0);
CreateText (GetLocStr (16001, 5));		{'Item #'}
textH := LNewObj;
defaultFontIDNo := GetTextFont (textH, 0);
defaultFontStyle := GetTextStyle (textH, 0);
```
```python
import vs

# Procedure GetTextStyle returns the text style at a specified position
# within the referenced text object.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer
Position = 1

resultN = vs.GetTextStyle(TextHd, Position)
vs.Message('GetTextStyle returned: ' + str(resultN))
```

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
