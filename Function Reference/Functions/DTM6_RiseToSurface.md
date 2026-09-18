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

## Examples
```pascal
boo := DTM6_RiseToSurface( dtmHand, tmpH, kCurrentDTM, 1 );
```
```python
import vs

# Modifies the passed object so it lies on the surface of the desired DTM.
hDTMObject = vs.FSActLayer()  # handle to the first selected object on the active layer
hObject = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
TINType = 0
sendType = 0

ok = vs.DTM6_RiseToSurface(hDTMObject, hObject, TINType, sendType)
if ok:
    vs.Message('DTM6_RiseToSurface succeeded')
else:
    vs.Message('DTM6_RiseToSurface failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
