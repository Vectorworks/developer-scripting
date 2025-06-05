# SetPolyPt

## Description
Procedure SetPolyPt sets the location a specified vertex in the referenced polygon.

```pascal
PROCEDURE SetPolyPt(
				objectHd : HANDLE;
				index    : INTEGER;
				xR       : REAL;
				yR       : REAL);
```

```python
def vs.SetPolyPt(objectHd, index, xR, yR):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to polygon.|
|index|INTEGER|Index of vertex.|
|xR|REAL|New X coordinate of vertex.|
|yR|REAL|New Y coordinate of vertex.|

## Remarks
(Gerard Jonker, 2007 Jan. 8) Please have a look at my [http://www.vectorlab.info/index.php?title=Absolute_Origin comments on the VectorLab] regarding this function, concerning index and origin.

([[User:CBM-c-|_c_]], 2010 Dec. 25) From Raymond Mullin: ''It only works for Polygons, and not for Polylines.''. Using this function on polylines will rise an invalid handle warning. Please be careful on conversions from polygon to polyline through [ InsertVertex](InsertVertex.md) or other routines. See [ SetPolylineVertex](SetPolylineVertex.md). I thus remove the word ''polylines'' from the description above.

## See Also
For polygons:
* [GetPolyPt](GetPolyPt.md)

For polylines:
* [GetPolylineVertex](GetPolylineVertex.md)
* [SetPolylineVertex](SetPolylineVertex.md)

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
