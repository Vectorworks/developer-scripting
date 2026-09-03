# GetTextSize

## Description
Procedure GetTextSize returns the text point size at a specified position within the referenced text object. 1 point = 1/72&quot;. 

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

```pascal
FUNCTION GetTextSize(
				TextHd   : HANDLE;
				Position : INTEGER): REAL;
```

```python
def vs.GetTextSize(TextHd, Position):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Remarks
The result was previously an integer, but is now a floating point value.

Here's a snippet that shows how to get the text size that has been assigned to a PIO from the text menu:
```pascal
pioTextSize := ((GetObjectVariableReal(pioHandle, 17) / GetLScale(GetLayer(pioHandle))) * 72) / 25.4;
```

Example:
```pascal
PROCEDURE Example;
CONST
theSizeToSelect = 10;
VAR
criteria :STRING;

PROCEDURE SelectBySize(h :HANDLE);
BEGIN
IF GetTextSize(h, 0) = theSizeToSelect THEN SetSelect(h);
END;

BEGIN
DSelectAll;
criteria := '(T=10)';
ForEachObject(SelectBySize, criteria);
END;
RUN(Example);
```

## Examples
```pascal
IF not ValidNumStr( GetText( textFoundH ), t_real ) THEN BEGIN
	TextOrigin(0,0);
	CreateText(Concat(' ', KNNoteNo));
	SetTextFont( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextFont( textFoundH, 0 ) );
	SetTextSize( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextSize( textFoundH, 0 ) );
	SetTextStyle( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextStyle( textFoundH, 0 ) );
	AddNumberWidth := GetTextWidth( LNewObj );
	DelObject(LNewObj);
end ELSE AddNumberWidth := 0;

BEGIN
txtSize := GetTextSize(TmpTextHand,1);
txtSize := txtSize*(gTextSheetScale/100);
IF (gTextStyle = gsItemoverSheet) | (gTextStyle = gsItemSheet) THEN
	SetTextSize(TmpTextHand,(Len(txtStr)-Len(gSheetName)),Len(gSheetName),txtSize)
ELSE

10: BEGIN	{ Text }
	getTextOrientation(hTemp, x1, y1, startA, isMirr);
	FOR ptIndex := 0 TO len(gettext(hTemp))-1 DO setTextSize(hTemp, ptIndex, 1, factor*getTextSize(hTemp, ptIndex));
	setTextOrientation(hTemp, x1*factor, y1*factor, startA, isMirr);
	END;
```
```python
import vs

# Procedure GetTextSize returns the text point size at a specified position
# within the referenced text object.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer
Position = 1

value = vs.GetTextSize(TextHd, Position)
vs.Message('GetTextSize returned: ' + str(value))
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
