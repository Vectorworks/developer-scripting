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

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
