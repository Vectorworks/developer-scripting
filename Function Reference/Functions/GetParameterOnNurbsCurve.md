# GetParameterOnNurbsCurve

## Description
Given a NURBS curve handle and a point (in world space), this function returns the parameter of the point obtained by projecting the input point. The function also returns the index of the piece in the piecewise NURBS curve on which the projected point lies.

```pascal
FUNCTION GetParameterOnNurbsCurve(
				h                    : HANDLE;
				pointX,pointY,pointZ : REAL;
				VAR parameter        : REAL;
				VAR index            : LONGINT): BOOLEAN;
```

```python
def vs.GetParameterOnNurbsCurve(h, point):
    return (BOOLEAN, parameter, index)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|point|REAL|   |
|parameter|REAL|   |
|index|LONGINT|   |

## Examples
```pascal
resultOK := GetParameterOnNurbsCurve(h, 1.0, 2.0, 0.5, 1.5, 1);
```
```python
import vs

# Given a NURBS curve handle and a point (in world space), this function
# returns the parameter of the point obtained by projecting the input point.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
point = (0, 0)

ok, parameter, index = vs.GetParameterOnNurbsCurve(h, point)
vs.Message('GetParameterOnNurbsCurve returned: ' + str((ok, parameter, index)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
