# SetLayerDeltaZOffset

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

Sets the wall height's offset to the layer delta z.

```pascal
FUNCTION SetLayerDeltaZOffset(
				theWall           : HANDLE;
				layerDeltaZOffset : REAL): BOOLEAN;
```

```python
def vs.SetLayerDeltaZOffset(theWall, layerDeltaZOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|layerDeltaZOffset|REAL|The wall height's offset to the layer delta z.|

## See Also
VS Functions:
[GetLayerDeltaZOffset](GetLayerDeltaZOffset.md)

## Version
Availability: from VectorWorks12.5
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
