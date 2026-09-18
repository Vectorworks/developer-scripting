# GetTextFont

## Description
Procedure GetTextFont returns the font of the referenced text object at a specified position in the string.

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

```pascal
FUNCTION GetTextFont(
				objectHd : HANDLE;
				Position : INTEGER): INTEGER;
```

```python
def vs.GetTextFont(objectHd, Position):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Examples
#### VectorScript ####
```pascal
fontID:=GetTextFont(handleToText,2);
```
#### Python ####
```python
fontID = vs.GetTextFont(handleToText,2)
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

	{* Get Font *}
	SetObjectVariableInt(gParmH,28,GetObjectVariableInt(h,28));
	{* Get Style *}
	SetObjectVariableInt(gParmH,19,GetObjectVariableInt(h,19));
	tmp_i := GetFontID(GetFontName(GetTextFont(h,0)));
END;

BEGIN
	{get the documents default text font ID and style - these will be used to format the ws cells}
	createText ('0');
	defaultFontID := GetTextFont (LNewObj, 0);
	defaultFontStyle := GetTextStyle (LNewObj, 0);
	DelObject (LnewObj);
	IF (defaultFontStyle = 0) | (defaultFontStyle = 2) | (defaultFontStyle = 4) | (defaultFontStyle = 6) THEN
		boldFontStyle := defaultFontStyle + 1
```
```python
import vs

# Procedure GetTextFont returns the font of the referenced text object at a
# specified position in the string.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
Position = 1

resultN = vs.GetTextFont(objectHd, Position)
vs.Message('GetTextFont returned: ' + str(resultN))
```

## See Also
VS Functions:
[GetFontName](GetFontName.md) 
| [GetFontID](GetFontID.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
