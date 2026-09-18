# OLDGetDragSnapPoint

## Description
If the object has been dragged and snapped, the fuction will return TRUE and the point parameter will contain the snapping location.

```pascal
FUNCTION OLDGetDragSnapPoint(VAR point : VECTOR): BOOLEAN;
```

```python
def vs.OLDGetDragSnapPoint():
    return (BOOLEAN, point)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|point|VECTOR|   |

## Examples
```pascal
resultOK := OLDGetDragSnapPoint(point);
```
```python
import vs

# If the object has been dragged and snapped, the fuction will return TRUE
# and the point parameter will contain the snapping location.
ok, pt = vs.OLDGetDragSnapPoint()
vs.Message('OLDGetDragSnapPoint returned: ' + str((ok, pt)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
