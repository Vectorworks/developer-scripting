# GetLine

## Description
Procedure GetLine returns two user selected points, and draws a temporary &quot;rubberband&quot; line when prompting for the second point. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetLine(
				VAR p1X,p1Y : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetLine(callback):
    return none
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Returns coordinates of first user click.|
|p2|REAL|Returns coordinates of second user click.|

## Remarks
In Python this function will _NOT_ block execution. It will execute a callback function with the resulted line (two points as callback function parameters).

## Examples
on sample is similar to the sample in [GetPt](GetPt.md).

```pascal
BEGIN
	GetLine (x1, y1, x2, y2);
	c := Distance (x1, y1, x2, y2);
	IF c >= s THEN
	BEGIN
		isLine := TRUE;

regenStatus := GetCustomObjectInfo(parmName, parmHand, parmRecHand, wallHand);
IF ResourceIsOK THEN Initialize;{general setup, incl params}
ImportedNNASymbol := FALSE;
kNNAIDSymbol := GetPlugInString(7028);
GetLine(gX1,gY1,gX2,gY2);
IF Option THEN gExpert := TRUE;
If GetObject(kPIOName) = Nil then gExpert := FALSE; {Supress option on first insertion}
IF Command THEN BEGIN {swap ends}
	gXtemp := gX1;

GetLine( gx1, gy1, gx2, gy2 );
v1.x := gx1;
v1.y := gy1;
v2.x := gx2;
v2.y := gy2;
```
```python
import vs

# Procedure GetLine returns two user selected points, and draws a temporary
# &quot;rubberband&quot; line when prompting for the second point.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

callback = handle_object

vs.GetLine(callback)
```

## See Also
VS Functions:
[GetPt](GetPt.md) |
[GetPtL](GetPtL.md) |
[GetPt3D](GetPt3D.md) |
[GetPtL3D](GetPtL3D.md) |
[GetLine](GetLine.md) |
[GetLine3D](GetLine3D.md) |
[GetRect](GetRect.md) |
[GetRect3D](GetRect3D.md) |
[TrackObject](TrackObject.md)

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
