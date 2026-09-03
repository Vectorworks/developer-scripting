# GetTextWidth

## Description
Procedure GetTextWidth returns the margin width of the referenced text object.

```pascal
FUNCTION GetTextWidth(theText : HANDLE): REAL;
```

```python
def vs.GetTextWidth(theText):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Remarks
For wrapped blocks, the margin width is that set by the user. For unwrapped blocks, it is computed by VW to be the width of the longest line.

## Examples
```pascal
{determine the closer end of the text to the Group, as if text has a changed justification it is possible that}
{the origin might be on the further side of the text block or in its center!!!!}
{left justified text}
IF ( GetTextJust( textH ) = 1 ) THEN
	tempV := UnitVec( Ang2Vec( ang , 1) ) * GetTextWidth( textH ) + originVec
{right justified text}
ELSE IF ( GetTextJust( textH ) = 3 ) THEN tempV := UnitVec( Ang2Vec( ang + 180 , 1) ) * GetTextWidth( textH ) + originVec
{center justified text}
else BEGIN
	tempV := UnitVec( Ang2Vec( ang , 1) ) * GetTextWidth( textH )/2 + originVec;
	originVec := UnitVec( Ang2Vec( ang + 180 , 1) ) * GetTextWidth( textH )/2 + originVec;
END;

BEGIN
	CreateText( DetailText );
	Offset := GetTextWidth( LNewObj );
	DelObject( LNewObj );

{find the a second tangent where the text object should end}
IF doingLowerFloor THEN boo := PointAlongPoly(pathOfTravelPoly, (travelPerim/20) + GetTextWidth(LNewObj), ptTxtNext, tangentPt1)
ELSE boo := PointAlongPoly(pathOfTravelPoly, travelPerim - (travelPerim/20) - GetTextWidth(LNewObj), ptTxtNext, tangentPt1);
tangentPt := (tangentPt + tangentPt1) * 0.5;
```
```python
import vs

# Procedure GetTextWidth returns the margin width of the referenced text object.
theText = 'Example text'

value = vs.GetTextWidth(theText)
vs.Message('GetTextWidth returned: ' + str(value))
```

## See Also
VS Functions:
[SetTextWidth](SetTextWidth.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
