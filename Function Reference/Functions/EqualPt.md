# EqualPt

## Description
Function EqualPt returns whether the two specified coordinate locations are equal (i.e., the same point, to 12 significant digits).

```pascal
FUNCTION EqualPt(
				p1X,p1Y : REAL;
				p2X,p2Y : REAL): BOOLEAN;
```

```python
def vs.EqualPt(p1, p2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Coordinates of first comparison point.|
|p2|REAL|Coordinates of second comparison point.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
x1, y1, x2, y2 :REAL;
BEGIN
x1 := 1;
y1 := 1;
x2 := 1.0000000000001;
y2 := 1.0000000000001;
Message(EqualPt(x1, y1, x2, y2));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	x1 = 1
	y1 = 1
	x2 = 1.0000000000001
	y2 = 1.0000000000001
	vs.Message(vs.EqualPt(x1, y1, x2, y2))
Example()
```

## See Also
VS Functions:
* [EqPt](EqPt.md)
* [EqPt2D](EqPt2D.md)
* [EqPt3D](EqPt3D.md)

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
