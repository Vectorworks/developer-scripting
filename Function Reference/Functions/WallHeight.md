# WallHeight

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

Procedure WallHeight returns the wall heights of the referenced wall object.

```pascal
PROCEDURE WallHeight(
				wallHd      : HANDLE;
				VAR startHt : REAL;
				VAR endHt   : REAL);
```

```python
def vs.WallHeight(wallHd):
    return (startHt, endHt)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|startHt|REAL|Returns start height of wall.|
|endHt|REAL|Returns end height of wall.|

## Version
Availability: from MiniCAD6.0
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
