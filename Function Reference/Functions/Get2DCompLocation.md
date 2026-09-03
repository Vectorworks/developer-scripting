# Get2DCompLocation

```pascal
PROCEDURE Get2DCompLocation(
				hObject          : HANDLE;
				component        : INTEGER;
				VAR onBoundsCube : BOOLEAN;
				VAR offset       : REAL);
```

```python
def vs.Get2DCompLocation(hObject, component):
    return (onBoundsCube, offset)
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
Get2DCompLocation(hObject, 1, TRUE, 1.0);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
component = 1

onBoundsCube, offset = vs.Get2DCompLocation(hObject, component)
vs.Message('Get2DCompLocation returned: ' + str((onBoundsCube, offset)))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
