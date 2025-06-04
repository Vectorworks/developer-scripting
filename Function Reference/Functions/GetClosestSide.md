# GetClosestSide

## Description
Returns the indices of the vertices that define the side closest to the specified location.  

GetClosestSide supports only 2D objects.  If the object is unsupported, -1 will be returned as the index values.

```pascal
PROCEDURE GetClosestSide(
				obj        : HANDLE;
				ptX,ptY    : REAL;
				VAR index1 : INTEGER;
				VAR index2 : INTEGER);
```

```python
def vs.GetClosestSide(obj, pt):
    return (index1, index2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|pt|REAL|Coordinates of location.|
|index1|INTEGER|Index of first vertex of closest side.|
|index2|INTEGER|Index of second vertex of closest side.|

## Remarks
[[User:CBM-c-| _c_]], 2021.12.28: If applied to polylines, the routine is unreliable for poly segments whose type is NOT corner: it fails. So basically this works well only on polygons

[[User:CBM-c-| _c_]], 2011.12.31: If applied to polygons, the routine needs the passed point to be ON a side. It will return different values depending if
* the chosen point is ON the side: always returns the vertexes defining the found side
* the chosen point is NOT ON the side: 
** polygons: returns the range of vertexes --> 1-(count of vertexes)
** polylines: returns the range of vertexes --> (count of vertexes) -(count of vertexes)

## Version
Availability: from VectorWorks 8.5

## Category
* [Utility](../Categories/Utility.md)
