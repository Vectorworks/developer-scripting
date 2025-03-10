# HWallHeight

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See architectural category for replacement:
:[[VS:DelObjStoryBound|DelObjStoryBound]]
:[[VS:DelObjStoryBounds|DelObjStoryBounds]]
:[[VS:GetObjBoundElevation|GetObjBoundElevation]]
:[[VS:GetObjStoryBound|GetObjStoryBound]]
:[[VS:GetObjStoryBoundsAt|GetObjStoryBoundsAt]]
:[[VS:GetObjStoryBoundsCnt|GetObjStoryBoundsCnt]]
:[[VS:GetStoryLayerInfo|GetStoryLayerInfo]]
:[[VS:HasObjStoryBound|HasObjStoryBound]]
:[[VS:HasObjStoryBounds|HasObjStoryBounds]]
:[[VS:SetObjectStoryBound|SetObjectStoryBound]]

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
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* Objects - Walls

