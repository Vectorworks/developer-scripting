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

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
