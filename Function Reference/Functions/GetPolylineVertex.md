# GetPolylineVertex

## Description
Returns information about the specified polyline vertex.

Note that vertexNum is 1-based for Polygons and Polylines, and 0-based for 3D Polylines.

```pascal
PROCEDURE GetPolylineVertex(
				obj            : HANDLE;
				vertexNum      : INTEGER;
				VAR pX,pY      : REAL;
				VAR vertexType : INTEGER;
				VAR arcRadius  : REAL);
```

```python
def vs.GetPolylineVertex(obj, vertexNum):
    return (p, vertexType, arcRadius)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|vertexNum|INTEGER|Index of vertex to be queried.|
|p|REAL|X-Y coordinates of vertex.|
|vertexType|INTEGER|Type of vertex: 0 - Corner, 1 - Bezier, 2 - Cubic, 3 - Arc, 4 - Radius|
|arcRadius|REAL|Radius of vertex corner (arc vertex only).|

## Remarks
(*\_c\_*, 2022.01.18) In VS Python this routine will always return a 2-items tuple, clipping it if "necessary". If you need a 3 items tuple for usage in vs.Vec2Ang, for example, you will need to restore the third item.
```python
# test GetPolylineVertex
p = (0, 0, 0)
vs.AlrtDialog( 'init tuple: ' + str(len(p)) ) # 3 items
p, vertexType, arcRadius = vs.GetPolylineVertex(vs.FSActLayer(), 1) # take care to have a polygon selected
vs.AlrtDialog( 'after GetPolylineVertex: ' + str(len(p)) ) # 2 items?!?
```

(Charles Chandler, 2001 Jun. 11) The radius value can be one of three things: 
* 0, in which case the actual drawn radius is simply the biggest radius that will fit, 
* the same as the actual displayed radius, 
* larger than the displayed radius, in which case the drawn radius is the biggest radius that will fit.

MaKro 2022:
* 4 - Radius (new type has been added) [GetPolylineArcMaxRadius](GetPolylineArcMaxRadius.md)
* Corner vertex, which has no radius at all, returns value other than zero for radius, so always check vertex type.
* For an Arc type (3) vertex, the internally stored radius can be different to the one showed in the info palette. [ConvertToArcPolyline](ConvertToArcPolyline.md) fixes this issue.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    obj        : HANDLE;
    vertexNum  : INTEGER;
    ptX, ptY   : REAL;
    vertexType : INTEGER;
    arcRadius  : REAL;

BEGIN
    obj := FSActLayer;
    FOR vertexNum := 1 TO GetVertNum(obj) DO BEGIN
        GetPolylineVertex(obj, vertexNum, ptX, ptY, vertexType, arcRadius);
        TextOrigin(ptX, ptY);
        CreateText(Concat('vNum: ', vertexNum, '  vType: ', vertexType, '  radius: ', arcRadius));
    END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
    obj = vs.FSActLayer()
    for vertexNum in range( 1, vs.GetVertNum(obj) ):
        ptVt, vertexType, arcRadius = vs.GetPolylineVertex( obj, vertexNum )
        vs.TextOrigin( ptVt[0], ptVt[1] )
        vs.CreateText( vs.Concat('vNum: ', vertexNum, '  vType: ', vertexType, '  radius: ', arcRadius) )

Example()
```

```pascal
BEGIN
	GetPolylineVertex(lineHandle, vertexNum, x, y, GetVertexType, radius);
END;

if arrowLineH <> NIL then BEGIN {TEXT NOTE (STRAIGHT)}
	{BRACE TYPE Group}
	if polyH <> NIL then BEGIN
		{find the vertex in the middle of the imaginery Line connecting th ends of the Poly}
		GetPolylineVertex( polyH, 1, v1[1], v1[2], verttype, arcrad );
		GetPolylineVertex( polyH, 7, v2[1], v2[2], verttype, arcrad );
		tempV := v1 - v2;
		tempV := UnitVec( tempV );
		tempV := tempV * Norm(v1 - v2)/2;

FOR vertexNum := 1 TO GetVertNum( tempPolyH ) DO BEGIN
	GetPolylineVertex( tempPolyH, vertexNum, pX, pY, vertexType, arcRadius );
	InsertVertex( polylineH, pX, pY, 1, vertexType, arcRadius );
	SetVertexVisibility( polylineH, 1, TRUE );
END;
```
```python
import vs

# Returns information about the specified polyline vertex.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
vertexNum = 1

p, vertexType, arcRadius = vs.GetPolylineVertex(obj, vertexNum)
vs.Message('GetPolylineVertex returned: ' + str((p, vertexType, arcRadius)))
```
See also in tutorials: [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md), [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

## See Also
For polylines:
* [SetPolylineVertex](SetPolylineVertex.md)
* [GetPolylineArcMaxRadius](GetPolylineArcMaxRadius.md)

For polygons:
* [GetPolyPt](GetPolyPt.md)
* [SetPolyPt](SetPolyPt.md)

## Version
Availability: from VectorWorks 8.5

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
