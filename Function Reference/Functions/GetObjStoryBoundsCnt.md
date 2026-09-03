# GetObjStoryBoundsCnt

## Description
Return the number of story bounds defined for this object.

```pascal
FUNCTION GetObjStoryBoundsCnt(obj : HANDLE): INTEGER;
```

```python
def vs.GetObjStoryBoundsCnt(obj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|

## Examples
```pascal
resultN := GetObjStoryBoundsCnt(obj);
```
```python
import vs

# Return the number of story bounds defined for this object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetObjStoryBoundsCnt(obj)
vs.Message('GetObjStoryBoundsCnt returned: ' + str(resultN))
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
