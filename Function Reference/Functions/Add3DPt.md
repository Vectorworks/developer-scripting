# Add3DPt

## Description
Procedure Add3DPt adds a vertex into a newly created 3D polygon.

Calls to Add3DPt should be made between calls to BeginPoly3D, which initiates polygon creation, and EndPoly3D, which terminates polygon creation. A minimum of two vertices must be created to define a valid 3D polygon object, and calculations may be performed within the BeginPoly3D-EndPoly3D structure, providing additional options for vertex generation.

```pascal
PROCEDURE Add3DPt(pX,pY,pZ : REAL);
```

```python
def vs.Add3DPt(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Location of 3D vertex.|

## Examples
#### VectorScript ####
```pascal
BeginPoly3D;
Add3DPt(0,0,0);
Add3DPt(2,0,0);
Add3DPt(2,2,0);
Add3DPt(1,3,0);
Add3DPt(0,2,0);
Add3DPt(0,0,0);
EndPoly3D;
```
#### Python ####
```python
vs.BeginPoly3D()
vs.Add3DPt(0,0,0)
vs.Add3DPt(2,0,0)
vs.Add3DPt(2,2,0)
vs.Add3DPt(1,3,0)
vs.Add3DPt(0,2,0)
vs.Add3DPt(0,0,0)
vs.EndPoly3D()
```

```pascal
IF (hPolygon <> NIL) THEN BEGIN
	BeginPoly3D;
	FOR i := 1 TO getvertnum(hPolygon) DO BEGIN
		GetPolyPt(hPolygon,i,x,y);
		Add3DPt(x,y,0);
		END;

BEGIN
	GetPolyPt (LNewObj, k, x, y);
	Add3DPt(x, y, 0);
END;

{Draw 3D Poly.}
BeginPoly3D;
	for cnt := 1 to vertex_cnt DO Add3DPt(vertices[cnt].x, vertices[cnt].y, 0);
EndPoly3D;
SetFPat(LNewObj, 0);
```
```python
if drawing3D:
	vs.Add3DPt( v2.x, v2.y, z )

if ( useModifiers ):
	vs.BeginPoly3D()
	vs.Add3DPt( 0, width + vs.PCurb_Width + gDTM, 0 )
	vs.Add3DPt( length, width + vs.PCurb_Width + gDTM, vs.PRise )
	vs.Add3DPt( length, -( width + vs.PCurb_Width + gDTM ), vs.PRise )
	vs.Add3DPt( 0, -( width + vs.PCurb_Width + gDTM ), 0 )
	vs.EndPoly3D()

guterCurb = vs.PGutter_Width
vs.ClosePoly()
vs.BeginPoly3D()
vs.Add3DPt( -vs.PCurb_Width, 0, vs.PRise )
vs.Add3DPt( -( radiusFromEdge - ( radiusFromEdge * vs.Cos( sweepTmp ) ) ), ( radiusFromEdge * vs.Sin( sweepTmp ) - vs.PCurb_Width - ( vs.PCurb_Width * ( 1 - ( vs.Tan( sweepTmp / 2 ) ) ) ) ), 0 )
vs.Add3DPt( -( radiusFromEdge - ( radiusFromEdge * vs.Cos( sweepTmp ) ) ), radiusFromEdge * vs.Sin( sweepTmp ), 0 )
vs.Add3DPt( -( radiusFromEdge - ( radiusFromEdge * vs.Cos( sweepTmp ) ) ), radiusFromEdge * vs.Sin( sweepTmp ) + guterCurb, 0 )
vs.Add3DPt( vs.PThroat_Width + radiusFromEdge - ( radiusFromEdge * vs.Cos( sweepTmp ) ), radiusFromEdge * vs.Sin( sweepTmp ) + guterCurb, 0 )
```

## See Also
VS Functions:
[BeginPoly3D](BeginPoly3D.md) 
| [EndPoly3D](EndPoly3D.md)

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
