# DTM6_GetDTMOver

## Description
Gets the DTM over (geometrically) a specified object.

```pascal
FUNCTION DTM6_GetDTMOver(hObject : HANDLE): HANDLE;
```

```python
def vs.DTM6_GetDTMOver(hObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|A handle of the object under which geometry a Site Model is to be searched.|

## Examples
```pascal
resultH := DTM6_GetDTMOver(hObject);
```
```python
import vs

# Gets the DTM over (geometrically) a specified object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.DTM6_GetDTMOver(hObject)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
[DTM6_GetDTMObject](DTM6_GetDTMObject.md)

## Version
Availability: from Vectorworks 2011

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
