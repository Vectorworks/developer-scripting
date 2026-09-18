# DelObjStoryBound

## Description
Delete the specified story bounds from this object.

```pascal
PROCEDURE DelObjStoryBound(
				obj     : HANDLE;
				boundID : INTEGER);
```

```python
def vs.DelObjStoryBound(obj, boundID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|boundID|INTEGER|The identifier of the story bound.|

## Examples
```pascal
BEGIN
	DelObjStoryBound( gPluginH, kTopBoundArchitID );
	DelObjStoryBound( gPluginH, kBotBoundArchitID );
	SetLegacyObjectBounds( gPluginName, gPluginH, 'ArchHeightInfo', pOA_Height, kTopBoundArchitID, kBotBoundArchitID, 0.0 );
```
```python
import vs

# Delete the specified story bounds from this object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
boundID = 1

vs.DelObjStoryBound(obj, boundID)
```

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
