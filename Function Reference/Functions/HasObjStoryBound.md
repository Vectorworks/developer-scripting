# HasObjStoryBound

## Description
Determine if the object has the specified story bound ID present.

```pascal
FUNCTION HasObjStoryBound(
				obj     : HANDLE;
				boundID : INTEGER): BOOLEAN;
```

```python
def vs.HasObjStoryBound(obj, boundID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|boundID|INTEGER|The identifier of the story bound.|

## Examples
```pascal
IF ( NOT HasObjStoryBound( gPluginH, kOldTopBoundArchitID ) ) THEN
BEGIN
	UpdateBound( formatHand, gPluginH, kOldTopBoundArchitID, kOldTopBoundArchitID, pOA_Height );
END;

BEGIN
	formatHand := GetObject( objectName );
	IF GetObjStoryBound( formatHand, topBoundID, boundType, boundStory, layerLevelType, topOffset ) &
		( NOT HasObjStoryBound( objectHand, topBoundID ) ) THEN
	BEGIN
		SetObjectStoryBound( objectHand, topBoundID, boundType, boundStory, layerLevelType, topOffset );
	END;
```
```python
import vs

# Determine if the object has the specified story bound ID present.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
boundID = 1

ok = vs.HasObjStoryBound(obj, boundID)
if ok:
    vs.Message('HasObjStoryBound succeeded')
else:
    vs.Message('HasObjStoryBound failed')
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
