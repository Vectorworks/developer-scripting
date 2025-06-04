# GetLinkHeightToLayerDeltaZ

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

Returns whether or not the wall's height is linked to the layer delta z.

```pascal
FUNCTION GetLinkHeightToLayerDeltaZ(theWall : HANDLE): BOOLEAN;
```

```python
def vs.GetLinkHeightToLayerDeltaZ(theWall):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|

## See Also
VS Functions:
[SetLinkHeightToLayerDeltaZ](SetLinkHeightToLayerDeltaZ.md)

## Version
Availability: from VectorWorks12.5
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
