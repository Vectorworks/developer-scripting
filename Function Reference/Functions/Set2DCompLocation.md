# Set2DCompLocation

```pascal
FUNCTION Set2DCompLocation(
				hObject      : HANDLE;
				component    : INTEGER;
				onBoundsCube : BOOLEAN;
				offset       : REAL): BOOLEAN;
```

```python
def vs.Set2DCompLocation(hObject, component, onBoundsCube, offset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|component|INTEGER|   |
|onBoundsCube|BOOLEAN|   |
|offset|REAL|   |

## Examples
```pascal
resultOK := Set2DCompLocation(hObject, 1, TRUE, 1.0);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
component = 1
onBoundsCube = True
offset = 0.0

ok = vs.Set2DCompLocation(hObject, component, onBoundsCube, offset)
if ok:
    vs.Message('Set2DCompLocation succeeded')
else:
    vs.Message('Set2DCompLocation failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
