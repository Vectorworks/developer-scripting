# Get2DPt

## Description
Returns the location of the specified vertex of a referenced object.

```pascal
PROCEDURE Get2DPt(
				obj           : HANDLE;
				index         : INTEGER;
				VAR locX,locY : REAL);
```

```python
def vs.Get2DPt(obj, index):
    return loc
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|index|INTEGER|Index of vertex to be queried (range of 1 to n)|
|loc|REAL|Coordinates of 2D vertex  location.|

## Remarks
([[User:CBM-c-|_c_]], 2007.05.27): Used with bounding box objects without vertexes (groups...), the routine doesn't throw error and always returns the coordinates of the center, independently of the passed vertex index.

(RGM Feb 2006): This will generally return the center of an object. Use [[VS:GetSymLoc| GetSymLoc]] if you want eg. the 'point' of a Point PIO.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
    p : VECTOR;
BEGIN
    IF FSActLayer = NIL THEN
        AlrtDialog( 'Select a polygon or a polyline' )
    ELSE BEGIN { here you might want to check if it's a valid object type }
        Get2DPt( FSActLayer, 2, p.x, p.y ); { stores in p the coordinates of vtx 2 }
        Locus( p.x, p.y );
    END;
END;
Run(Example);
```
==== Python ====
```python
if vs.FSActLayer() == None:
    vs.AlrtDialog( 'Select a polygon or a polyline' )
else:
    p = vs.Get2DPt( vs.FSActLayer(), 2 ) # stores in p the coordinates of vtx 2
    vs.Locus( p[0], p[1] )
```

## See Also
VS Functions:
* [GetPolyPt](GetPolyPt.md)
* [GetPolyPt3D](GetPolyPt3D.md)
* [GetPolylineVertex](GetPolylineVertex.md)

## Version
Availability: from VectorWorks 8.5

## Category
* [Object Info](../Categories/Object%20Info.md)
