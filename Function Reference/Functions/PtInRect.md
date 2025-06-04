# PtInRect

## Description
Function PtInRect returns whether the coordinate location is located within the specified rectangular boundary.

```pascal
FUNCTION PtInRect(
				pointX,pointY : REAL;
				rect1X,rect1Y : REAL;
				rect2X,rect2Y : REAL): BOOLEAN;
```

```python
def vs.PtInRect(point, rect1, rect2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|point|REAL|X-Y coordinate point location.|
|rect1|REAL|Top left coordinate of rectangular area.|
|rect2|REAL|Bottom right coordinate of rectangular area.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
pointX, pointY, rect1X, rect1Y, rect2X, rect2Y :REAL;
BEGIN
pointX := 1;
pointY := 1;
rect1X := 0;
rect1Y := 2;
rect2X := 2;
rect2Y := 0;
Message(PtInRect(pointX, pointY, rect1X, rect1Y, rect2X, rect2Y));
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
