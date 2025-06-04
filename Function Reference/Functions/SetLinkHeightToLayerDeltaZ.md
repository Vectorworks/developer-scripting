# SetLinkHeightToLayerDeltaZ

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

Sets whether or not the wall's height is linked to the layer delta z.

```pascal
FUNCTION SetLinkHeightToLayerDeltaZ(
				theWall           : HANDLE;
				linkToLayerDeltaZ : BOOLEAN): BOOLEAN;
```

```python
def vs.SetLinkHeightToLayerDeltaZ(theWall, linkToLayerDeltaZ):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|linkToLayerDeltaZ|BOOLEAN|Whether or not the wall's height is linked to the layer delta z.|

## See Also
VS Functions:
[GetLinkHeightToLayerDeltaZ](GetLinkHeightToLayerDeltaZ.md)

## Version
Availability: from VectorWorks12.5
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
