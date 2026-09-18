# GetFontID

## Description
Function GetFontID converts the string name of an available font to a font ID which can be passed to other VectorScript routines.

```pascal
FUNCTION GetFontID(fontName : STRING): INTEGER;
```

```python
def vs.GetFontID(fontName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fontName|STRING|Name of installed font.|

## Remarks
returns -1 if the requested font is not available

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
str :STRING;
BEGIN
str := StrDialog('Enter the font name:', 'Arial');
AlrtDialog(Concat('The font ID is: ', GetFontID(str)));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	str = vs.StrDialog('Enter the font name:', 'Arial')
	vs.AlrtDialog(vs.Concat('The font ID is: ', vs.GetFontID(str)))

Example()
```

```pascal
BEGIN
	getData := FALSE;
	createErrorMessage2( errorText, kErrMsgTextSize, GetFontID( kErrMsgTextFont ), kErrMsgWidth, gX0, gY0, kBeep );
	HRotate( LNewObj, gX0, gY0, -GetSymRot( gPluginH ) );
END

BeginText;
	str
EndText;
tmpH := LNewObj;
SetTextFont( tmpH, 0, GetTextLength( tmpH ) , GetFontID( tmpStruct.NotesFormat.font ) );
SetTextSize( tmpH, 0, GetTextLength( tmpH ) , tmpStruct.NotesFormat.size );
SetTextStyle( tmpH, 0, GetTextLength( tmpH ) , tmpStruct.NotesFormat.style );
SetRField( gnH, kGeneralNotes, kCPt2x, Num2Str( realPrecision, GetTextWidth( tmpH ) ) );
DelObj( tmpH );

fieldVal := GetRField(parmH, parmN, fieldN);
if version >= 1000 then BEGIN
	SetRField(parmH, parmN, fieldN, GetFontName(GetObjectVariableInt(parmH, 28)));
end else IF (fieldVal <> '') THEN BEGIN
	SetObjectVariableInt(parmH, 28, GetFontID(fieldVal));
	TextFont(GetFontID(fieldVal));
END;
```
```python
import vs

# Function GetFontID converts the string name of an available font to a font
# ID which can be passed to other VectorScript routines.
fontName = 'Arial'

resultN = vs.GetFontID(fontName)
vs.Message('GetFontID returned: ' + str(resultN))
```
See also in tutorials: [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md), [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
