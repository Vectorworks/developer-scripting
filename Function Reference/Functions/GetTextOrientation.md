# GetTextOrientation

## Description
Procedure GetTextOrientation returns the position and orientation attributes of the referenced text object.

```pascal
PROCEDURE GetTextOrientation(
				theText                     : HANDLE;
				VAR textOriginX,textOriginY : REAL;
				VAR textAng                 : REAL;
				VAR textIsMirrored          : BOOLEAN);
```

```python
def vs.GetTextOrientation(theText):
    return (textOrigin, textAng, textIsMirrored)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|textOrigin|REAL|Returns coordinates of text origin.|
|textAng|REAL|Returns rotation angle of text.|
|textIsMirrored|BOOLEAN|Returns mirror state of text.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
theText :HANDLE;
textOriginX, textOriginY, textAng :REAL;
textIsMirrored :BOOLEAN;
BEGIN
theText := FSActLayer;
GetTextOrientation(theText, textOriginX, textOriginY, textAng, textIsMirrored);
Locus(textOriginX, textOriginY);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	theText = vs.FSActLayer()
	textOriginPt, textAng, textIsMirrored = vs.GetTextOrientation ( theText )
	vs.Locus(textOriginPt[0], textOriginPt[1])

Example()
```

```pascal
IF ( NOT arrTBlocksUsed[ tbNUm ] ) THEN
	{check if text and Group are in same Layer}
	if GetLayer( objH ) = GetLayer( textH ) then BEGIN
		{get the text origin position and rotation Angle}
		GetTextOrientation( textH, originVec[1], originVec[2], ang, mirrored );
		{determine the closer end of the text to the Group, as if text has a changed justification it is possible that}
		{the origin might be on the further side of the text block or in its center!!!!}
		{left justified text}
		IF ( GetTextJust( textH ) = 1 ) THEN

SetTextVertAlignN(LNewObj, tVAlign);
SetTextJustN(LNewObj, tJust);
SetTextSpace(LNewObj, 2);
SetFPat(LNewObj,0);
GetTextOrientation(LNewObj, ptX, ptY, angle, isMirrored);
{Move the text object at the correct location}
HMove(LNewObj, x + SizeFactor - ptX, y - ptY);
Draw_text_block  := LNewObj;
SetPrefInt(83, gVAlign);

10: BEGIN	{ Text }
	getTextOrientation(hTemp, x1, y1, startA, isMirr);
	FOR ptIndex := 0 TO len(gettext(hTemp))-1 DO setTextSize(hTemp, ptIndex, 1, factor*getTextSize(hTemp, ptIndex));
	setTextOrientation(hTemp, x1*factor, y1*factor, startA, isMirr);
	END;
```
```python
import vs

# Procedure GetTextOrientation returns the position and orientation
# attributes of the referenced text object.
theText = 'Example text'

textOrigin, textAng, textIsMirrored = vs.GetTextOrientation(theText)
vs.Message('GetTextOrientation returned: ' + str((textOrigin, textAng, textIsMirrored)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
