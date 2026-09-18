# Wall

## Description
Procedure Wall creates a wall object in a VectorWorks document. The wall will adopt the current default settings for walls when created.

```pascal
PROCEDURE Wall(
				p1X,p1Y : REAL;
				p2X,p2Y : REAL);
```

```python
def vs.Wall(p1, p2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Start point of wall.|
|p2|REAL|End point of wall.|

## Remarks
[sd 8/18/98]

## Examples
```pascal
Wall(-(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi));
SetObjExpandTexture(lNewObj,FALSE);
SetTextureRef(lNewObj,-1,7);
WallCap(FALSE,FALSE,FALSE,-3*upi,3*upi);
WallCap(TRUE,FALSE,FALSE,3*upi,-3*upi);

BEGIN
	Wall(PolyPoints[I+1].pt.x,PolyPoints[I+1].pt.y,PolyPoints[I].pt.x,PolyPoints[I].pt.y);
	PolyPoints[I].h := LNewObj;
END;

end else BEGIN {create a new wall as no old one on this layer is close enough to be reshaped}
	Wall(PolyPoints[I].pt.x,PolyPoints[I].pt.y,PolyPoints[I+1].pt.x,PolyPoints[I+1].pt.y);
	PolyPoints[I].h := LNewObj;
END;
```
```python
import vs

# Procedure Wall creates a wall object in a VectorWorks document.
p1 = (0, 0)
p2 = (2, 2)

vs.Wall(p1, p2)
newObj = vs.LNewObj()  # handle to the newly created object
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## See Also
VS Functions:
[RoundWall](RoundWall.md)

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
