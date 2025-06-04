# GetPolyPt3D

## Description
Procedure GetPolyPt3D returns the coordinates of the specified vertex of the referenced mesh, 3D polygon, or NURBS curve object.

Error checking for valid index values must be provided by the programmer.

```pascal
PROCEDURE GetPolyPt3D(
				objectHd     : HANDLE;
				index        : INTEGER;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.GetPolyPt3D(objectHd, index):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to 3D mesh or polygon.|
|index|INTEGER|Index of vertex (range of 0 to n-1).|
|p|REAL|Returns 3D coordinates of vertex.|

## Remarks
Conrad Preen, 2014/10/12: Save you the trip to VectorLab, index is zero-based and points returned w.r.t. internal origin.

Gerard Jonker, 2007/1/8:  Please have a look at my [http://www.vectorlab.info/index.php?title=Absolute_Origin comments on the VectorLab] regarding this function, concerning index and origin.

[[User:CBM-c-|_c_]], 2010/09/12: Warning: From VW13 this function returns the z-value adding the layer Z. So, for example, by a layer z of 10, if you have a vertex whose z is 1, the routine will return 11.

## Examples
==== VectorScript ====
```pascal
FOR i := 0 to (GetVertNum(thePoly) - 1) DO
    GetPolyPt3D(thePoly, i, vertX, vertY, vertZ);
```
==== Python ====
```python
def Example():
    obj = vs.FSActLayer()
    for vertexNum in range(1, vs.GetVertNum(obj)):
        ptVt = vs.GetPolyPt3D(obj, vertexNum)
        vs.TextOrigin(ptVt[0], ptVt[1], ptVt[2])
        vs.CreateText(vs.Concat('vNum: ', vertexNum))
Example()
```

## See Also
VS Functions:
* [Get2DPt](Get2DPt.md)
* [GetPolyPt](GetPolyPt.md)
* [GetPolylineVertex](GetPolylineVertex.md)

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
