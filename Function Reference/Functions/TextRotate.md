# TextRotate

## Description
Procedure TextRotate sets the angle of a new text object.

```pascal
PROCEDURE TextRotate(Rotation : REAL);
```

```python
def vs.TextRotate(Rotation):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Rotation|REAL|Rotation angle, in degrees, for text.|

## Examples
#### VectorScript ####
```pascal
TextRotate(45);
TextOrigin(0&quot;,0&quot;);
CreateText('Rotated string');
```
#### Python ####
```python

```

```pascal
if ((tmpAngle <= -90) AND (tmpAngle >= -180)) THEN
	tmpAngle := 180 + tmpAngle
else if ((tmpAngle <= 180) AND (tmpAngle > 90)) THEN
	tmpAngle := tmpAngle - 180;
TextRotate(tmpAngle);
TextJust(2);
TextOrigin(ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2]);

TextSize (gCellLabelSize);
PushAttrs;
{TextFace ([bold]);}
TextFlip (0);
TextRotate (#0);
TextSpace (2);
TextJust (2);
TextVerticalAlign (3);
FillPat (kFPat0);

SetLSN(lnewobj,CheckLSN(-lineStyle));
HRotate(lnewobj,x,y,-rot);
TextJust(2);
TextVerticalAlign(3);
IF pRotateText THEN TextRotate(-rot) ELSE TextRotate(tRot);
TextSize(pItem_Text_Size);
TextOrigin(xC,yC);
CreateText(concat(pprfx,itemTag));
hText := lnewobj;
```
```python
vs.TextRotate(Rotation)
```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
