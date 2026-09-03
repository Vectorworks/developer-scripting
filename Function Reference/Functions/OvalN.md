# OvalN

## Description
Creates an oval with the specified bounds.

```pascal
PROCEDURE OvalN(
				orginX,orginY         : REAL;
				directionX,directionY : REAL;
				width                 : REAL;
				height                : REAL);
```

```python
def vs.OvalN(orgin, direction, width, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|orgin|REAL|   |
|direction|REAL|   |
|width|REAL|   |
|height|REAL|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
OvalN(0, 0, 1, 0, 1, 1);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
BeginGroup;
	OvalN (0-LegProfRadius, 0-LegProfRadius, 90, 0, LegProfRadius*2, LegProfRadius*2);
    LegProfileH := LNewObj;
	SetFPat (LegProfileH,1);
	SetFillFore(LegProfileH,kBmpAModR,kBmpAModG,kBmpAModB);
	SetFillBack(LegProfileH,kBmpAModR,kBmpAModG,kBmpAModB);

OvalN (SubPoleCentX-PoleRadius, SubPoleCentY-PoleRadius, 90, 0, PoleRadius*2, PoleRadius*2);

{Far Left - Q1}
OvalN(CurveLx,FarDispDistCurrent,90,0,-CurveLx*2,(CurveLy-FarDispDistCurrent)*2);
DispQ1 := LNewObj;
```
```python
vs.OvalN(orgin, direction, 1.0, 2.0)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
