# GetTextLength

## Description
GetTextLength returns the string length of the referenced text object.

```pascal
FUNCTION GetTextLength(TextHd : HANDLE): INTEGER;
```

```python
def vs.GetTextLength(TextHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|

## Examples
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

CreateText(GetPluginString(3002));
textHandle := LNewObj;
textLength := GetTextLength(textHandle);

SetTextSize( TextObjHand, 0, LEN( GetText( LNewObj ) ), 10 );
}
SetTextJust( TextObjHand, 2 );
SetTextVerticalAlign( TextObjHand, 3 );
SetTextFont( TextObjHand, 0, GetTextLength( LNewObj ), GetFontID( pioFontName ) );
SetTextStyle( TextObjHand, 0, GetTextLength( LNewObj ), 1 );
```
```python
import vs

# GetTextLength returns the string length of the referenced text object.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetTextLength(TextHd)
vs.Message('GetTextLength returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
