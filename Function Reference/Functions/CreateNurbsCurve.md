# CreateNurbsCurve

## Description
Creates a new NURBS curve in the document.

```pascal
FUNCTION CreateNurbsCurve(
				firstX,firstY,firstZ : REAL;
				byCtrlPts            : BOOLEAN;
				degree               : INTEGER): HANDLE;
```

```python
def vs.CreateNurbsCurve(first, byCtrlPts, degree):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|first|REAL|Coordinates of the first point in the curve definiton.|
|byCtrlPts|BOOLEAN|Create curve by control points (not interpolation).|
|degree|INTEGER|The degree of the NURBS curve.|

## Remarks
Creates a NURBS curve with a single fit or control point, if it succeeds, return nil if it fails.

([[User:CBM-c-|_c_]], 2010.12.26) Large [http://www.cs.mtu.edu/~shene/COURSES/cs3621/NOTES/ introduction to NURBS] by C.-K. Shene (MTU), including great many images.

## Examples
==== VectorScript ====
```pascal
PROCEDURE NewNurbsCurve;
VAR
nC :HANDLE;
BEGIN
nC := CreateNurbsCurve(0, 0, 0, true, 2);
AddVertex3D(nC, 1, 1, 0);
AddVertex3D(nC, 2, 0, 0);
END;
RUN(NewNurbsCurve);
```
==== Python ====
```python
def NewNurbsCurve():
	nC = vs.CreateNurbsCurve(0, 0, 0, True, 2)
	vs.AddVertex3D(nC, 1, 1, 0)
	vs.AddVertex3D(nC, 2, 0, 0)

NewNurbsCurve()
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
