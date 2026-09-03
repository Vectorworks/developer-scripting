# WallCap

## Description
Procedure WallCap creates a wall cap on a newly created wall object.

Specifying nonzero values for the cap offset values will create angled wall caps.

```pascal
PROCEDURE WallCap(
				atStart          : BOOLEAN;
				closed           : BOOLEAN;
				round            : BOOLEAN;
				rightOffDistance : REAL;
				leftOffDistance  : REAL);
```

```python
def vs.WallCap(atStart, closed, round, rightOffDistance, leftOffDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|atStart|BOOLEAN|Start-end location of wall cap.|
|closed|BOOLEAN|Controls display status of cap.|
|round|BOOLEAN|Specifies flat or round cap.|
|rightOffDistance|REAL|Right extension of wall line beyond end point.|
|leftOffDistance|REAL|Left extension of wall line beyond end point.|

## Examples
#### VectorScript ####
```pascal
Wall(0,0,7',0);
WallCap(True, True, False, 1.0', 0.0);
{sets the cap status of the starting cap of the wall as flat cap, bevelled, with the right side extending 1' beyond the wall end point}
```
#### Python ####
```python

```

```pascal
Wall(-(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi));
SetObjExpandTexture(lNewObj,FALSE);
SetTextureRef(lNewObj,-1,7);
WallCap(FALSE,FALSE,FALSE,-3*upi,3*upi);
WallCap(TRUE,FALSE,FALSE,3*upi,-3*upi);
result := SetWallOverallHeights(lnewobj,0,0,'',cHeight,0,0,'',cHeight);
WallPeak((cWidth/2-3*upi),cRise+cHeight);
ResetObject(lNewObj);
```
```python
vs.WallCap(atStart, closed, round, 1.0, 2.0)
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
