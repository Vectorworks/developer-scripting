# HWallHeight

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>. See architectural category for replacement:
:[DelObjStoryBound](DelObjStoryBound.md)
:[DelObjStoryBounds](DelObjStoryBounds.md)
:[GetObjBoundElevation](GetObjBoundElevation.md)
:[GetObjStoryBound](GetObjStoryBound.md)
:[GetObjStoryBoundsAt](GetObjStoryBoundsAt.md)
:[GetObjStoryBoundsCnt](GetObjStoryBoundsCnt.md)
:[GetStoryLayerInfo](GetStoryLayerInfo.md)
:[HasObjStoryBound](HasObjStoryBound.md)
:[HasObjStoryBounds](HasObjStoryBounds.md)
:[SetObjectStoryBound](SetObjectStoryBound.md)

Procedure HWallHeight sets the wall heights of the referenced wall object.

```pascal
PROCEDURE HWallHeight(
				wallHd              : HANDLE;
				startHeightDistance : REAL;
				endHeightDistance   : REAL);
```

```python
def vs.HWallHeight(wallHd, startHeightDistance, endHeightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|startHeightDistance|REAL|New start height of wall.|
|endHeightDistance|REAL|New end height of wall.|

## Remarks
You can also change the various heights of the wall with SetObjectVariableReal function calls.

604 StartHeightTop
605 StartHeightBottom
606 EndHeightTop
607 EndHeightBottom

## Version
Availability: from MiniCAD6.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
