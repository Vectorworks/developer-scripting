# EqualRect

## Description
Function EqualRect returns whether the two specified rectangular areas are equal.

```pascal
FUNCTION EqualRect(
				rectAp1X,rectAp1Y : REAL;
				rectAp2X,rectAp2Y : REAL;
				rectBp1X,rectBp1Y : REAL;
				rectBp2X,rectBp2Y : REAL): BOOLEAN;
```

```python
def vs.EqualRect(rectAp1, rectAp2, rectBp1, rectBp2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|rectAp1|REAL|Top left coordinate of rectangle A.|
|rectAp2|REAL|Bottom right coordinate of rectangle A.|
|rectBp1|REAL|Top left coordinate of rectangle B.|
|rectBp2|REAL|Bottom right coordinate of rectangle B.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
Message(EqualRect(0,0,3,3,3,3,0,0));
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	vs.Message(vs.EqualRect(0,0,3,3,3,3,0,0))
Example()
```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
