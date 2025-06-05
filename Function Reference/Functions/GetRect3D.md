# GetRect3D

## Description
Procedure GetRect3D draws a temporary &quot;rubberband&quot; 3D rectangle on the working plane. The user defines the rectangle by selecting two points which define the top left and bottom right of the rectangle. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetRect3D(
				VAR p1x, p1y, p1z : REAL;
				VAR p2x, p2y, p2z : REAL;
				useWP             : BOOLEAN);
```

```python
def vs.GetRect3D(useWP, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1x, p1y, p1z|REAL|Returns coordinates of first user click.|
|p2x, p2y, p2z|REAL|Returns coordinates of second user click.|
|useWP|BOOLEAN|TRUE if the returned point have to be on the active Working Plane. Snapping to arbitrary 3D geometry will produce vertical projection result on the WP; FALSE if the point can be arbitrary 3D point (produced, for example, by snapping to a 3D geometry)|

## Remarks
In Python this function will <b>NOT</b> block execution. It will execute a callback function with the resulted rectangle (two points as callback function parameters).

## Examples
on sample is similar to the sample in [GetPt](GetPt.md).

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
Availability: from Vectorworks 2010

## Category
* [User Interactive](../Categories/User%20Interactive.md)
