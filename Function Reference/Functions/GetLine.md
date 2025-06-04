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
In Python this function will <b>NOT</b> block execution. It will execute a callback function with the resulted line (two points as callback function parameters).

## Examples
on sample is similar to the sample in [[VS:GetPt]].

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
