# NurbsDelVertex

## Description
Deletes a point in the referenced NURBS curve or surface. The function deletes the index2 point of the index1 piece for nurbs curve or it deletes an entire index2 row (index1 = 1) or column (index1 = 0) of points.

```pascal
PROCEDURE NurbsDelVertex(
				objectHd : HANDLE;
				index1   : LONGINT;
				index2   : LONGINT);
```

```python
def vs.NurbsDelVertex(objectHd, index1, index2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index1|LONGINT|V-index of point in NURBS surface. The index is zero based.|
|index2|LONGINT|Index of point in NURBS curve, or U-index of a point in NURBS surface. The index is zero based.|

## Remarks
This function will work for both nurbs curves and nurbs surfaces.

[DelObject](DelObject.md) should be used to completely remove a NURBS curve or surface from the drawing.

There is also a bug in that VW does not redraw properly after a NurbsDelVertex call.

Create a simple nurbs curve, run it, and double click the pan tool to see it working:
```pascal
NurbsDelVertex(FSActLayer, 0, 0);
```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
