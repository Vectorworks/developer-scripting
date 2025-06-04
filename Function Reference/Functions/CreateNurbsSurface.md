# CreateNurbsSurface

## Description
Creates a new NURBS surface in the document. The surface has two directions, denoted u and v. The surface acts like a set of NURBS curves in each direction, with the number of control points and the degree specified in the parameter list. (Note that the degree parameters have to be lower than the numPts parameters.)

After creating the surface, you must set the location of each of the control points with NurbsSetPt3D, and when you are done call ResetBBox to make sure the bounding box is correct.

```pascal
FUNCTION CreateNurbsSurface(
				numUPts : LONGINT;
				numVPts : LONGINT;
				uDegree : INTEGER;
				vDegree : INTEGER): HANDLE;
```

```python
def vs.CreateNurbsSurface(numUPts, numVPts, uDegree, vDegree):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|numUPts|LONGINT|The number of definition points along the u-axis of the surface.|
|numVPts|LONGINT|The number of definition points along the v-axis of the surface.|
|uDegree|INTEGER|Degree of the NURBS curve in the u direction.|
|vDegree|INTEGER|Degree of the NURBS curve in the v direction.|

## Remarks
returns a handle to the newly created NURBS surface if it succeeds,  return NULL if it fails

Creates a NURBS surface with the number of control points and degrees as specified. Call NurbsSetPt3D() to set the control net

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := CreateNurbsSurface(3, 3, 1, 1);
NurbsSetPt3D(h, 0, 0, 0, 0, 0);
NurbsSetPt3D(h, 0, 1, 1, 0, 0);
NurbsSetPt3D(h, 0, 2, 2, 0, 0);
NurbsSetPt3D(h, 1, 0, 0, 1, 0);
NurbsSetPt3D(h, 1, 1, 1, 1, 1);
NurbsSetPt3D(h, 1, 2, 2, 1, 0);
NurbsSetPt3D(h, 2, 0, 0, 2, 0);
NurbsSetPt3D(h, 2, 1, 1, 2, 0);
NurbsSetPt3D(h, 2, 2, 2, 2, 0);
ResetBBox(h);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	h = vs.CreateNurbsSurface(3, 3, 1, 1)
	vs.NurbsSetPt3D(h, 0, 0, 0, 0, 0)
	vs.NurbsSetPt3D(h, 0, 1, 1, 0, 0)
	vs.NurbsSetPt3D(h, 0, 2, 2, 0, 0)
	vs.NurbsSetPt3D(h, 1, 0, 0, 1, 0)
	vs.NurbsSetPt3D(h, 1, 1, 1, 1, 1)
	vs.NurbsSetPt3D(h, 1, 2, 2, 1, 0)
	vs.NurbsSetPt3D(h, 2, 0, 0, 2, 0)
	vs.NurbsSetPt3D(h, 2, 1, 1, 2, 0)
	vs.NurbsSetPt3D(h, 2, 2, 2, 2, 0)
	vs.ResetBBox(h)
Example()
```

## See Also
VS Functions:
[NurbsSurfaceEvalPt](NurbsSurfaceEvalPt.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
