# Add2DVertex

## Description
This procedure will add to a polyline a vertex defined by its position, its type(0 to 4) and the radius if type is 3 or 4. A vertex of type 4 should be followed and preceded by corner vertices. If the type is equal to 4, the point will be a middle point of an arc. In this case if the radius is not given (0) it will be computed.

```pascal
PROCEDURE Add2DVertex(
				pX, pY     : REAL;
				vertexType : INTEGER;
				arcRadius  : REAL);
```

```python
def vs.Add2DVertex(p, vertexType, arcRadius):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|The vertex to add to a polyline.|
|vertexType|INTEGER|The type of the vertex it could be 0, 1, 2, 3 or 4.|
|arcRadius|REAL|The arc radius if the vertex type is 3 or 4.|

## Remarks
*\_c\_* (2020.09.28): 
Vertex types:
: 0 = corner
: 1 = bezier
: 2 = cubic
: 3 = arc
: 4 = radius

## Examples
```pascal
beginPoly;
Add2DVertex(0,0,0,0);
Add2DVertex(1,1,4,0);
Add2DVertex(2,0,0,0);
Add2DVertex(3,1,4,0);
Add2DVertex(4,0,0,0);
endPoly;
```

```pascal
BeginGroup;
BeginPoly;
  MoveTo(-0.050871161717227",-0.047391266048944");
  LineTo(-0.050871161717227",-0.172590948885572");
  Add2DVertex(-0.000871161717227",-0.222590948885572",4,0.05");
  LineTo(0.049128838282773",-0.172590948885572");
  LineTo(0.049068611093032",-0.020137565169201");
  Add2DVertex(0.044328302938945",-0.001213194214057",4,0.05");
  LineTo(-0.000871161717227",0.027409051114428");

BEGIN
	OpenPoly;
	BeginPoly;
		Add2DVertex( startPoint.x, startPoint.y, 0, 0 );
		Add2DVertex( pt2.x, pt2.y, 1, 0 );
		Add2DVertex( pt4.x, pt4.y, 1, 0 );
		Add2DVertex( endPoint.x, endPoint.y, 0, 0 );
	EndPoly;

	AddPoint(pt2.x, pt2.y);
	AddPoint(pt3.x, pt3.y);
end else FOR i := 1 TO GetVertNum(h) DO BEGIN
	GetPolylineVertex(h, i, x, y, t, r);
	Add2DVertex(x, y, t, r);
END;
```
```python
import vs

# This procedure will add to a polyline a vertex defined by its position, its
# type(0 to 4) and the radius if type is 3 or 4.
p = (0, 0)
vertexType = 0
arcRadius = 1.0

vs.Add2DVertex(p, vertexType, arcRadius)
newObj = vs.LNewObj()  # handle to the newly created object
```
See also in tutorials: [03. Build a Curved Path with Mixed Vertex Types](ai%20examples/03_CurvedPolylinePath.md), [19. Cubic Bezier Sampled to a Polyline](ai%20examples/19_BezierPolylineSampling.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
