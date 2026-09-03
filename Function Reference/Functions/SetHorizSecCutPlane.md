# SetHorizSecCutPlane

```pascal
FUNCTION SetHorizSecCutPlane(
				hObject        : HANDLE;
				objectCutPlane : INTEGER): BOOLEAN;
```

```python
def vs.SetHorizSecCutPlane(hObject, objectCutPlane):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|objectCutPlane|INTEGER|   |

## Examples
```pascal
resultOK := SetHorizSecCutPlane(hObject, 1);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
objectCutPlane = 1

ok = vs.SetHorizSecCutPlane(hObject, objectCutPlane)
if ok:
    vs.Message('SetHorizSecCutPlane succeeded')
else:
    vs.Message('SetHorizSecCutPlane failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
