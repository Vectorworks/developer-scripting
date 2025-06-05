# DTM6_IsObjectReady

## Description
Checks if this passed DTM object is ready for use. That means that the object has associated internal data (triangulated data and so which doesn't allow the document to be big). If this returns false, you can call [ ResetObject](ResetObject.md) to prepare the object to be used.

As of Vectorworks 2011 this function will always return true.

```pascal
FUNCTION DTM6_IsObjectReady(hDTMObject : HANDLE): BOOLEAN;
```

```python
def vs.DTM6_IsObjectReady(hDTMObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|   |

## Version
Availability: all versions.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
