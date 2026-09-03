# SetPlanarTransform

## Description
Get planar matrix and transform polygon points.

```pascal
FUNCTION SetPlanarTransform(h : HANDLE): HANDLE;
```

```python
def vs.SetPlanarTransform(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
planRotation := GetPrefReal(93);
tempobjH := HDuplicate (pathTemplate, 0, 0);
tempobjH := SetPlanarTransform(tempobjH);
HCenter (tempobjH, x0, y0);
HMove(tempobjH, -x0, -y0);
gPluginObjH := CreateCustomObjectN (objType, x0, y0, -planRotation, FALSE);
HRotate(tempObjH, 0, 0, planRotation);
```
```python
import vs

# Get planar matrix and transform polygon points.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.SetPlanarTransform(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Utility](../Categories/Utility.md)
