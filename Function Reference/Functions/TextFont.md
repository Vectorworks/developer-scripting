# TextFont

## Description
Procedure TextFont sets the active font for the document.

```pascal
PROCEDURE TextFont(fontID : INTEGER);
```

```python
def vs.TextFont(fontID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fontID|INTEGER|Font ID setting for document.|

## Examples
#### VectorScript ####
```pascal
TextFont(GetFontID('Times'));
```
#### Python ####
```python

```

```pascal
if version >= 1000 then BEGIN
	SetRField(parmH, parmN, fieldN, GetFontName(GetObjectVariableInt(parmH, 28)));
end else IF (fieldVal <> '') THEN BEGIN
	SetObjectVariableInt(parmH, 28, GetFontID(fieldVal));
	TextFont(GetFontID(fieldVal));
END;

  if( typeIntComp = -1 ) | ( typeIntStyle = -1 ) | ( typeIntArrow = -1 ) THEN BEGIN
defaultFont := GetPrefString(100);  { save default font and set back after OK pressed }
GetVersion(major, minor, maintenance, platform);
if (platform = 1) then { Macintosh = 1; Windows = 2 }
	TextFont(0)	{ set default font to the application font }
else
	TextFont(-1);
ALLOCATE layers [1..NumLayers];
layerCnt := 0;
h := FLayer;
for cnt := 1 to NumLayers do BEGIN

BEGIN
	PushAttrs;
	TextFont( GetFontID( GetLocStr (12028, 4) ) );
	TextSize( 48 );
	x := x2 - ((borderWidth + blockWidth/2));
	y := y2 + ((borderWidth + blockWidth/2));
	TextVerticalAlign(3);
```
```python
vs.TextFont(fontID)
```
See also in tutorials: [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
