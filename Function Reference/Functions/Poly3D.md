# Poly3D

## Description
Procedure Poly3D creates a three dimensional polygon in a VectorWorks document. The vertices of the polygon are specified by a list of parameters x1, y1, z1 through xn, yn, and zn, which specify the coordinate locations of each vertex.

```pascal
PROCEDURE Poly3D(p : REAL);
```

```python
def vs.Poly3D(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Examples
#### VectorScript ####
```pascal
Poly3D(1,1,0,1.5,1.5,1,2.5,1.5,1,);
```
#### Python ####
```python

```

```pascal
{ added component subclassing [04-30-01 CRH]}
{ revised component subclassing [04-3-02 KMH]}
ChangeToClass(gStepStyle.strClassActualName);
IF simple THEN
	Poly3d(cix,ciy,h,	cox,coy,h,		c2ox,c2oy,h,	c2ix,c2iy,h)
ELSE BEGIN
	BeginXtrd(h,h-pthickness);
	Poly(cix,ciy,cox,coy,c2ox,c2oy,c2ix,c2iy);
	EndXtrd;
END;

MoveTo(position_x, position_y);
IF gShow3D THEN BEGIN
	MoveTo(numSpaces*sLength, #0);
	PenLoc(term_x, term_y);
	Poly3D(position_x, position_y, kZ_FACTOR, term_x, term_y, kZ_FACTOR);
	MoveTo(position_x, position_y);
END;

{front}
Poly3D(	 thick, -dpth,shelf, wdth - thick,-dpth,shelf,
		 wdth - thick,-dpth, pbottom, thick,-dpth, pbottom);
```
```python
vs.Poly3D((0, 0))
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
