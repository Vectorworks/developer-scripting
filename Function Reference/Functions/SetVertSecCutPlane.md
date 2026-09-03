# SetVertSecCutPlane

```pascal
FUNCTION SetVertSecCutPlane(
				hObject        : HANDLE;
				objectCutPlane : INTEGER): BOOLEAN;
```

```python
def vs.SetVertSecCutPlane(hObject, objectCutPlane):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|objectCutPlane|INTEGER|   |

## Examples
```pascal
resultOK := SetVertSecCutPlane(hObject, 1);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
objectCutPlane = 1

ok = vs.SetVertSecCutPlane(hObject, objectCutPlane)
if ok:
    vs.Message('SetVertSecCutPlane succeeded')
else:
    vs.Message('SetVertSecCutPlane failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
