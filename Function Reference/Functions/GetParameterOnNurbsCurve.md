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

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
