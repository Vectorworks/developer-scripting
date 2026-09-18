# NurbsCurveType

## Description
Returns the curve type of a segment of the referenced NURBS curve.

The index is zero based (0 to number of segments - 1).

```pascal
PROCEDURE NurbsCurveType(
				objectHd    : HANDLE;
				index       : LONGINT;
				VAR isByFit : BOOLEAN);
```

```python
def vs.NurbsCurveType(objectHd, index):
    return isByFit
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve.|
|index|LONGINT|Index of curve segment.|
|isByFit|BOOLEAN|Type of curve segment.|

## Examples
```pascal
NurbsCurveType(objectHd, 1, TRUE);
```
```python
import vs

# Returns the curve type of a segment of the referenced NURBS curve.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

result = vs.NurbsCurveType(objectHd, index)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
