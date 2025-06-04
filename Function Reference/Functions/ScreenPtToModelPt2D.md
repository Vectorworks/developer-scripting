# ScreenPtToModelPt2D

## Description
Transforms a point from screen coordinate in plan rotation to the model coordinates.

```pascal
PROCEDURE ScreenPtToModelPt2D(VAR pX, pY : REAL);
```

```python
def vs.ScreenPtToModelPt2D(p):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pX|REAL|Input output parameter. X Coordinate of the point to be translated.|
|pY|REAL|Input output parameter. Y Coordinate of the point to be translated.|

## Remarks
Takes into account both translation and rotation.

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
