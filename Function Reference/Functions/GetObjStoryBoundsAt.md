# GetObjStoryBoundsAt

## Description
Return the story bound ID of the specified story bound index. The index is between 1 and the result of GetObjStoryBoundsCnt.

```pascal
FUNCTION GetObjStoryBoundsAt(
				obj   : HANDLE;
				index : INTEGER): INTEGER;
```

```python
def vs.GetObjStoryBoundsAt(obj, index):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|
|index|INTEGER|Index of the story bound which ID will be returned. This index should be between 1 and the result of GetObjStoryBoundsCnt.|

## Examples
```pascal
resultN := GetObjStoryBoundsAt(obj, 1);
```
```python
import vs

# Return the story bound ID of the specified story bound index.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

resultN = vs.GetObjStoryBoundsAt(obj, index)
vs.Message('GetObjStoryBoundsAt returned: ' + str(resultN))
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
