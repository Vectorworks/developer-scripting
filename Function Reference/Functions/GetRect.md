# GetRect

## Description
Procedure GetRect draws a temporary &quot;rubberband&quot; rectangle onscreen, similar to a selection marquee. The user defines the rectangle by selecting two points which define the top left and bottom right of the rectangle. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetRect(
				VAR p1X,p1Y : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetRect(callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Returns coordinates of first user click.|
|p2|REAL|Returns coordinates of second user click.|

## Remarks
In Python this function will _NOT_ block execution. It will execute a callback function with the resulted rectangle (two points as callback function parameters).

## Examples
on sample is similar to the sample in [GetPt](GetPt.md).

```pascal
BEGIN
	GetRect(x1, y1, x2, y2);
	IF x2 = x1 THEN x2 := x1 + 100;
	IF y2 = y1 THEN y2 := y1 + 100;

GetRect(x1, y1, x2, y2);
IF x1 >= x2 THEN x2 := x1 + 100;
IF y1 <= y2 THEN y2 := y1 - 100;
```
```python
import vs

# Procedure GetRect draws a temporary &quot;rubberband&quot; rectangle
# onscreen, similar to a selection marquee.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

callback = handle_object

vs.GetRect(callback)
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
