# Locus

## Description
Procedure Locus creates a 2D locus object at the specified coordinate location.

```pascal
PROCEDURE Locus(pX,pY : REAL);
```

```python
def vs.Locus(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate location of new locus.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
x, y :REAL;
BEGIN
HCenter(FSActLayer, x, y);
Locus(x, y);
END;
RUN(Example);
```
#### Python ####
```python
x = 100
y = 0
vs.Locus (x, y)
```

```pascal
BeginMxtrd(cHeight+cRoof_Thickness,cHeight+cRoof_Thickness+cRise);
	Rect(-(cWidth/2+cOverhang),-(cWidth/2+cOverhang),(cWidth/2+cOverhang),(cWidth/2+cOverhang));
	Locus(0.0,0.0);
EndMxtrd;
SetTextureRef(lNewObj,-1,3);

Rise := Rise * ( 360 / angle );
L := angle * rise;
Absolute;
BeginSweep (180-angle, angle, kDt, -rise);
	Locus (radius + width/2 ,0);
	MoveTo (0, 0);
	Relative;
	Rect (0, 0 , width, -thk);
EndSweep;

BEGIN
	Absolute;
	Locus(-gShaftWidth/2,0.0);
	SetLW (LNewObj, 1);
	SetPenFore (LNewObj,65535,65535,65535);
	Locus(gShaftWidth/2,0.0);
	SetLW (LNewObj, 1);
```
```python
vs.Locus(0,0)
hTempLocus = vs.LNewObj()

vs.Locus((vs.PRadius+vs.PCurb_Width+(vs.PWidth/2)),0); SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gCurb_Class )
vs.EndSweep()

if ok:
	vs.Locus(center); SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gCurb_Class )
```
See also in tutorials: [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md), [12. Polygon Area and Centroid (Shoelace Formula)](ai%20examples/12_PolygonAreaCentroid.md), [13. Point-in-Polygon Test (Ray Casting)](ai%20examples/13_PointInPolygonRayCast.md), [15. Uniform Arc-Length Resampling of a Polyline](ai%20examples/15_PolylineResampleUniform.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
