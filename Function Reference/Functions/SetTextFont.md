# SetTextFont

## Description
Procedure SetTextFont sets the font of a substring in the referenced text object.

```pascal
PROCEDURE SetTextFont(
				objectHd : HANDLE;
				Start    : INTEGER;
				Count    : INTEGER;
				FontNum  : INTEGER);
```

```python
def vs.SetTextFont(objectHd, Start, Count, FontNum):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Start|INTEGER|Start position in text string.|
|Count|INTEGER|Length of substring.|
|FontNum|INTEGER|Font ID for substring.|

## Remarks
Note that "Start" is zero-based.

## Examples
#### VectorScript ####
```pascal
SetTextFont(handleToText,0,5,GetFontID('Helvetica'));

{sets the first five characters of the referenced text string to Helvetica}
```
#### Python ####
```python

```

```pascal
if ( KNsuffix = '' ) & ( KNprefix = GetText( textFoundH ) ) then BEGIN
	IF not ValidNumStr( GetText( textFoundH ), t_real ) THEN BEGIN
		TextOrigin(0,0);
		CreateText(Concat(' ', KNNoteNo));
		SetTextFont( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextFont( textFoundH, 0 ) );
		SetTextSize( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextSize( textFoundH, 0 ) );
		SetTextStyle( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextStyle( textFoundH, 0 ) );
		AddNumberWidth := GetTextWidth( LNewObj );
		DelObject(LNewObj);

IF ( objHand <> NIL ) THEN
	SetTextFont(LNewObj, 0, Len(text), GetObjectVariableInt(objHand, 28));

BEGIN
	SetTextFont (tempH, 0, Len (GetText (tempH)), GetObjectVariableInt (gPluginH, 28));
	SetTextStyle (tempH, 0, Len (GetText (tempH)), 0);
	SetTextStyle (tempH, 0, Len (GetText (tempH)), GetObjectVariableInt (gPluginH, 19));
END;
```
```python
vs.SetTextFont(objectHd, Start, 1, 2)
```

## See Also
VS Functions:
[GetFontID](GetFontID.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
