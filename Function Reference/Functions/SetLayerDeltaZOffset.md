# SetLayerDeltaZOffset

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
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
