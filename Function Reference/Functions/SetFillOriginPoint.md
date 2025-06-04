# SetFillOriginPoint

## Description
Sets the origin point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE SetFillOriginPoint(
				objectHandle : HANDLE;
				xOriginPoint : REAL;
				yOriginPoint : REAL);
```

```python
def vs.SetFillOriginPoint(objectHandle, xOriginPoint, yOriginPoint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xOriginPoint|REAL|X coordinate of origin point.|
|yOriginPoint|REAL|Y coordinate of origin point.|

## Examples
==== VectorScript ====
```pascal
SetFillOriginPoint(objectHandle, 10.0, 20.0);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
