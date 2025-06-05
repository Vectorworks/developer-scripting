# GetPt

## Description
Procedure GetPt switches the cursor to selection mode and allows the user to select a point in a VectorWorks document. This cannot be used if there is a function anywhere in the calling chain.

```pascal
PROCEDURE GetPt(VAR pX,pY : REAL);
```

```python
def vs.GetPt(callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Returns coordinates of mouse click.|
|callback|FUNCTION|Python only! A callback function that will be executed when the tool finishes. The callback receives the point|

## Remarks
In Python this function will _NOT_ block execution. It will execute a callback function with the resulted point.

[MaKro 6/2018]: ... in a tool consider using VS:vstGetCurrPt2D ...

## Examples
```pascal
PROCEDURE Example;
VAR
pt :POINT;
BEGIN
GetPt(pt.x, pt.y);
Message(pt);
END;
RUN(Example);
```
Python:
```python
import vs;

def DoIt(h1):
	vs.AlrtDialog( "we're in", h1 )

def PickPointCallback(pt):
	vs.ForEachObjectAtPoint(DoIt, 0, 0, pt[0], pt[1], 5)

vs.AlrtDialog( "show let you pick a point, and then show a dialog with the object's handle" )
vs.GetPt( PickPointCallback )
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
