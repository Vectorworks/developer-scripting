# DTM6_ClearModelCache

## Description
Clear the site model's cache.

```pascal
PROCEDURE DTM6_ClearModelCache(hObject : HANDLE);
```

```python
def vs.DTM6_ClearModelCache(hObject):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|A handle to the Site Model object.|

## Examples
```pascal
DTM6_ClearModelCache(hObject);
```
```python
import vs

# Clear the site model's cache.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.DTM6_ClearModelCache(hObject)
```

## See Also
[DTM6_GetDTMObject](DTM6_GetDTMObject.md)

## Version
Availability: from Vectorworks 2011

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
