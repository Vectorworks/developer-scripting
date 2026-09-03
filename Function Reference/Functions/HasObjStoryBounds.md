# HasObjStoryBounds

## Description
Determine if the object has any story bounds.

```pascal
FUNCTION HasObjStoryBounds(obj : HANDLE): BOOLEAN;
```

```python
def vs.HasObjStoryBounds(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object.|

## Examples
```pascal
resultOK := HasObjStoryBounds(obj);
```
```python
import vs

# Determine if the object has any story bounds.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.HasObjStoryBounds(obj)
if ok:
    vs.Message('HasObjStoryBounds succeeded')
else:
    vs.Message('HasObjStoryBounds failed')
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
