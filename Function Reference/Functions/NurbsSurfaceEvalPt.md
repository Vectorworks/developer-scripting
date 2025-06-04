# NurbsSurfaceEvalPt

## Description
This procedure determines the point on the nurbs surface at the given u,v values.

The u and v values can range from 0 to the value of the last knot in each direction.

```pascal
PROCEDURE NurbsSurfaceEvalPt(
				objectHd     : HANDLE;
				u            : REAL;
				v            : REAL;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.NurbsSurfaceEvalPt(objectHd, u, v):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to a NURBS surface.|
|u|REAL|Parameter between the minimum and maximum knot value in U direction.|
|v|REAL|Parameter between the minimum and maximum knot value in V direction.|
|p|REAL|Location of the u,v point on the surface.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE LocusSurface;
{ Create a surface, then put loci on it }
CONST
uMaxIndex   = 16;   { 17 points, 0 - 16 }
vMaxIndex   = 16;   { 17 points, 0 - 16 }
uDegree     = 3;    
vDegree     = 4;
xMin        = -3;
xMax        = 3;
yMin        = -3;
yMax        = 3;
zMax        = 3;
numLoci     = 17;
VAR
surfaceH                : HANDLE;
x,y,z,u,v               : REAL;
i,j                     : INTEGER;
numKnotsU, numKnotsV    : INTEGER;
maxFoundU, maxFoundV    : REAL;
uStep, vStep            : REAL;
BEGIN
{ Create a Nurbs Surface }

surfaceH := CreateNurbsSurface(uMaxIndex + 1, vMaxIndex + 1, uDegree, vDegree);
IF surfaceH &lt;&gt; NIL THEN BEGIN
FOR i := 0 TO uMaxIndex  DO BEGIN
FOR j := 0 TO vMaxIndex DO BEGIN
x := xMin + (xMax - xMin) * (i / uMaxIndex);
y := yMin + (yMax - yMin) * (j / vMaxIndex);
z := Cos(i - uMaxIndex / 2) *
Cos(j - vMaxIndex / 2) * 
zMax / (1 + x*x + y*y);
NurbsSetPt3D(surfaceH, i, j, x,y,z);
END;
END;
ResetBBox(surfaceH);

{ Add Loci }

{ Find number of knots in each direction }
numKnotsU := NurbsNumKnots(surfaceH, 1);
numKnotsV := NurbsNumKnots(surfaceH, 0);

{ Find the u and v real values that correspond the knots with the 
maximum u and v indices. }
NurbsKnot(surfaceH, 1, numKnotsU - 1, maxFoundU);       
NurbsKnot(surfaceH, 0, numKnotsV - 1, maxFoundV);       

Message(numKnotsU, ' ', numKnotsV);

{ Create 3D loci along each direction }
uStep   := maxFoundU / (numLoci - 1);
vStep   := maxFoundV / (numLoci - 1);

u := 0;
WHILE u &lt;= maxFoundU DO BEGIN
v := 0;
WHILE v &lt;= maxFoundV DO BEGIN
NurbsSurfaceEvalPt(surfaceH, u, v, x,y,z);
Locus3D(x,y,z);
v := v + vStep;
END;
u := u + uStep;
END;

{ Set View }
Projection(0,0,9.76,-4.88,4.88,4.88,-4.88);
SetView(#-45.0d,#-35.26438968275d,#-30.0d,0,0,0);
RedrawAll;
END;
END;
Run(LocusSurface);
```
==== Python ====
```python

```

## See Also
VS Functions:
[NurbsKnot](NurbsKnot.md) 
| [NurbsNumKnots](NurbsNumKnots.md)

## Version
Availability: from VectorWorks 9.5

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
