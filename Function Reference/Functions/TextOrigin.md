# TextOrigin

## Description
Procedure TextOrigin is used to specify the origin point (location) of a newly created text object.

The position of the actual text with respect to the origin is determined by the current vertical and horizontal text justification modes.

![Text Locus](files/Textlocus.gif)

```pascal
PROCEDURE TextOrigin(pX,pY : REAL);
```

```python
def vs.TextOrigin(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of text origin.|

## Examples
```pascal
else if ((tmpAngle <= 180) AND (tmpAngle > 90)) THEN
	tmpAngle := tmpAngle - 180;
TextRotate(tmpAngle);
TextJust(2);
TextOrigin(ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2]);

BEGIN
	TextOrigin(0,0);
	CreateText(Errors);
END;

BEGIN
	TextOrigin(pControlPoint01X, pControlPoint01Y);
	CreateText(pColumn_ID);
	SetTextVerticalAlign(LNewObj, 3);
	SetTextJust(LNewObj, 2);
```
```python
import vs

# Procedure TextOrigin is used to specify the origin point (location) of a
# newly created text object.
p = (0, 0)

vs.TextOrigin(p)
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md), [08. Attach and Read Records on Objects](ai%20examples/08_AttachAndReadRecords.md), [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md)

## See Also
VS Functions:
[MoveTo](MoveTo.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
