# SetWallHeights

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See architectural category for replacement:
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

Sets the wall heights of an unstyled wall. Will return false for a styled wall.

```pascal
FUNCTION SetWallHeights(
				h               : HANDLE;
				startHtDistance : REAL;
				endHtDistance   : REAL): BOOLEAN;
```

```python
def vs.SetWallHeights(h, startHtDistance, endHtDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|startHtDistance|REAL|   |
|endHtDistance|REAL|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
boo :BOOLEAN;
BEGIN
CallTool(-208);
h := FSActLayer;
boo := SetWallHeights(h, 12, 23);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
