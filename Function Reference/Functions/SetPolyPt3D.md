# SetPolyPt3D

## Description
Procedure SetPolyPt3D sets the position of the specified vertex in the referenced 3D object.

```pascal
PROCEDURE SetPolyPt3D(
				objectHd : HANDLE;
				index    : INTEGER;
				pX,pY    : REAL;
				zValue   : REAL);
```

```python
def vs.SetPolyPt3D(objectHd, index, p, zValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to mesh or 3D poly object.|
|index|INTEGER|Index of vertex point.|
|p|REAL|New X-Y coordinates of vertex.|
|zValue|REAL|New elevation of vertex.|

## Remarks
Please have a look at my [http://www.vectorlab.info/index.php?title=Absolute_Origin comments on the VectorLab] regarding this function, concerning index and origin.

[[User:Orso.b.schmid| Orso]], 2010/09/12: Warning: From VW13 this function subtracts the layer Z to the passed z-value. So, for example, by a layer z of 10, if you pass z=1 the vertex will go to -9.

## Examples
==== VectorScript ====
```pascal
SetPolyPt3D(objectHandle,3,2.5&quot;,3&quot;,8&quot;);
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
