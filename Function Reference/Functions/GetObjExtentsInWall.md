# GetObjExtentsInWall

## Description
Gets the extents of a Plugin object or symbol that is in a wall.  Returns the object's start point and end point along the wall line.

```pascal
FUNCTION GetObjExtentsInWall(
				symH                  : HANDLE;
				wallH                 : HANDLE;
				VAR startPtX,startPtY : REAL;
				VAR endPtX,endPtY     : REAL): BOOLEAN;
```

```python
def vs.GetObjExtentsInWall(symH, wallH):
    return (BOOLEAN, startPt, endPt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symH|HANDLE|   |
|wallH|HANDLE|   |
|startPt|REAL|   |
|endPt|REAL|   |

## Remarks
This currently fails on Round Walls: the subobject "symH" is found, but no points are returned. (VW 13.01+).

The values returned are relative to the wall start.
It works as expected on symbols and linear objects. If the object is a rectangular plug-in, the values returned are a little unexpected:
*"startPt" will be the center of the object, 
*"endPt" corresponds to start point + the width of the plug-in object. 
Thus endPt corresponds to the center of the plug-in object, if it has an horizontal flip in wall.

Julian [2009/08/30]
The values returned are in reference to the drawing origin, so you need to adjust those by subtracting the wall start point which can be obtained using GetSegPt1().

## Examples
```pascal
temp3_h := FIn3D(originalWall_h);
while temp3_h <> nil do BEGIN
	{Store the info for the symbols/PIOs in the walls.}
	if (GetType(temp3_h) = 15) | (GetType(temp3_h) = 86) then BEGIN
		if (GetObjExtentsInWall(temp3_h, originalWall_h, symStart.x, symStart.y, symEnd.x, symEnd.y) = true) then BEGIN
			GetSymLoc(temp3_h, symPt.x, symPt.y);
```
```python
import vs

# Gets the extents of a Plugin object or symbol that is in a wall.
symH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok, startPt, endPt = vs.GetObjExtentsInWall(symH, wallH)
vs.Message('GetObjExtentsInWall returned: ' + str((ok, startPt, endPt)))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
