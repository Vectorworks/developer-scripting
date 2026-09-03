# GetNurbsObjectDistanceFromPoint

## Description
Returns the distance from the input point  to the input NURBS Object h.

```pascal
FUNCTION GetNurbsObjectDistanceFromPoint(
				h             : HANDLE;
				pointX,pointY : REAL;
				VAR distance  : REAL): BOOLEAN;
```

```python
def vs.GetNurbsObjectDistanceFromPoint(h, point):
    return (BOOLEAN, distance)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a NURBS object.|
|point|REAL|point|
|distance|REAL|Distance between point and object.|

## Examples
```pascal
resultOK := GetNurbsObjectDistanceFromPoint(h, 1.0, 2.0, 0.5);
```
```python
import vs

# Returns the distance from the input point to the input NURBS Object h.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
point = (0, 0)

ok, distance = vs.GetNurbsObjectDistanceFromPoint(h, point)
vs.Message('GetNurbsObjectDistanceFromPoint returned: ' + str((ok, distance)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
