# SetTextStyle

## Description
Procedure SetTextStyle sets the text style of a specified substring in the referenced text object.

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
PROCEDURE SetTextStyle(
				objectHd : HANDLE;
				Start    : INTEGER;
				Count    : INTEGER;
				Style    : INTEGER);
```

```python
def vs.SetTextStyle(objectHd, Start, Count, Style):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Start|INTEGER|Start position in text string.|
|Count|INTEGER|Length of substring.|
|Style|INTEGER|Text style setting for substring.|

## Remarks
Note that SetTextStyle() toggles the bit you have set in the argument, but does not touch other bits (styles).  So if the text object is bold, italic, underline, outline, shadow and you call SetTextStyle(4) to attempt to set it to underline you will actually be turning the underline bit OFF and leaving the others alone. The resulting text is: bold, italic, outline, shadow.

Outline and Shadowed are only available on the Macintosh.

## Examples
#### VectorScript ####
```pascal
SetTextSyle(HandleToText, 0, 5, 34);

{set the style of the substring text to bold and shadowed}
```
#### Python ####
```python

```

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

str := gettext(textHandle);
IF NOT(pLabel) THEN
	settextstyle(texthandle,0,pos2,textStyleindex)
	{settextstyle(texthandle,0,textLength,textStyleindex)}

ELSE BEGIN
	IF pLStyle = kPlain 		THEN labelStyleIndex := 0
	ELSE IF pLStyle = kBold 	THEN labelStyleIndex := 1
	ELSE IF pLStyle = kItalic	THEN labelStyleIndex := 2
	ELSE labelStyleIndex := 3;

SetTextSize(textHandle, 0, textLength, 18);
SetTextStyle(textHandle, 0, textLength, 0);
```
```python
vs.SetTextStyle(objectHd, Start, 1, Style)
```

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
