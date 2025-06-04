# GetPtL

## Description
Procedure GetPtL creates a temporary &quot;rubberband&quot; line from a specified point to the user selected end point. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetPtL(
				p1X,p2Y     : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetPtL(callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Coordinates of line start point.|
|p2|REAL|Returns coordinates of mouse click.|

## Remarks
In Python this function will <b>NOT</b> block execution. It will execute a callback function with the resulted line (two points as callback function parameters).

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
pt1, pt2 :VECTOR;
BEGIN
GetPt(pt1.x, pt1.y);
GetPtL(pt1.x, pt1.y, pt2.x, pt2.y);
MoveTo(pt1.x, pt1.y);
LineTo(pt2.x, pt2.y);
END;
RUN(Example);
```
Python sample is similar to the sample in [[VS:GetPt]].
==== Python ====
```python

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
