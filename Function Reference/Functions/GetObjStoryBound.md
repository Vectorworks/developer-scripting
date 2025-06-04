# GetObjStoryBound

## Description
Get the data of the specified story bound of this object.

```pascal
FUNCTION GetObjStoryBound(
				obj                : HANDLE;
				boundID            : INTEGER;
				VAR boundType      : INTEGER;
				VAR boundStory     : INTEGER;
				VAR layerLevelType : STRING;
				VAR offset         : REAL): BOOLEAN;
```

```python
def vs.GetObjStoryBound(obj, boundID):
    return (BOOLEAN, boundType, boundStory, layerLevelType, offset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|boundID|INTEGER|The identifier of the story bound.|
|boundType|INTEGER|Bounding type: 0 - DefaultWallHeight; 1 - LayerZ; 2 - Story|
|boundStory|INTEGER|The story identified by 'boundType' = (2 - Story). If 'boundStory' = 0 then it is this story (the object's story); If 'boundStory' = 1 then it is the story above; If 'boundStory' = 2 then it is the story below.|
|layerLevelType|STRING|The layer type which defines this bound|
|offset|REAL|The offset distance from the specified bound story|

## See Also
VS Functions:
[HasObjStoryBounds](HasObjStoryBounds.md) 
| [HasObjStoryBound](HasObjStoryBound.md) 
| [GetObjStoryBound](GetObjStoryBound.md) 
| [SetObjectStoryBound](SetObjectStoryBound.md) 
| [DelObjStoryBounds](DelObjStoryBounds.md) 
| [DelObjStoryBound](DelObjStoryBound.md) 
| [GetObjStoryBoundsCnt](GetObjStoryBoundsCnt.md) 
| [GetObjStoryBoundsAt](GetObjStoryBoundsAt.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
