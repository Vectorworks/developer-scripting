# DTM6_RestoreDefaults

## Description
Sets the default settings for a Site model.

```pascal
PROCEDURE DTM6_RestoreDefaults(hObject : HANDLE);
```

```python
def vs.DTM6_RestoreDefaults(hObject):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
DTM6_RestoreDefaults(hObject);
```
```python
import vs

# Sets the default settings for a Site model.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.DTM6_RestoreDefaults(hObject)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
