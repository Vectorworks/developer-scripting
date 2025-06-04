# DTM6_RiseToSurface

## Description
Modifies the passed object so it lies on the surface of the desired DTM.

```pascal
FUNCTION DTM6_RiseToSurface(
				hDTMObject : HANDLE;
				hObject    : HANDLE;
				TINType    : INTEGER;
				sendType   : INTEGER): BOOLEAN;
```

```python
def vs.DTM6_RiseToSurface(hDTMObject, hObject, TINType, sendType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|   |
|hObject|HANDLE|   |
|TINType|INTEGER|   |
|sendType|INTEGER|   |

## Version
Availability: from Vectorworks 2014

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
