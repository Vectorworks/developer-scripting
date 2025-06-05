# GetPtL3D

## Description
Procedure GetPtL3D creates a temporary &quot;rubberband&quot; 3D line from a specified point to the user selected end point. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetPtL3D(
				p1        : REAL;
				VAR p2    : REAL;
				useWPOnly : BOOLEAN);
```

```python
def vs.GetPtL3D(useWPOnly, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Coordinates of line start point.|
|p2|REAL|Returns coordinates of mouse click.|
|useWPOnly|BOOLEAN|TRUE if the returned point have to be on the active Working Plane. Snapping to arbitrary 3D geometry will produce vertical projection result on the WP; FALSE if the point can be arbitrary 3D point (produced, for example, by snapping to a 3D geometry)|

## Remarks
In Python this function will _NOT_ block execution. It will execute a callback function with the resulted line (two points as callback function parameters).

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
