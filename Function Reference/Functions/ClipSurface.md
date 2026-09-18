# ClipSurface

## Description
Creates a new surface object by subtracting the intersection of surfaces s1 and s2 from s1.

```pascal
PROCEDURE ClipSurface(
				s1 : HANDLE;
				s2 : HANDLE);
```

```python
def vs.ClipSurface(s1, s2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s1|HANDLE|Handle to object.|
|s2|HANDLE|Handle to object.|

## Remarks
ClipSurface is not reliable if the smaller poly is not fully contained within the larger one.

Note that in the above example, PrevObj(h2); was used to get a handle to the clipped surface. Also note that checking the validity of this handle and possibly even its object type (polyline) or comparing it to the object being clipped (IF h3 <> h1), is necessary to check that the clipping operation was successful.

## Examples
#### VectorScript ####
```pascal
PROCEDURE ClipSurfaceExample;
VAR
h1, h2, h3 :HANDLE;
BEGIN
DSelectAll;
CallTool(-203);
h1 := FSActLayer;
DSelectAll;
CallTool(-203);
h2 := FSActLayer;
ClipSurface(h1, h2);
h3 := PrevObj(h2);
IF h3 <> h1 THEN SetFPat(h3, 5);
END;
RUN(ClipSurfaceExample);
```
#### Python ####
```python
def ClipSurfaceExample():
	vs.DSelectAll()
	vs.CallTool(-203)
	h1 = vs.FSActLayer()
	vs.DSelectAll()
	vs.CallTool(-203)
	h2 = vs.FSActLayer()
	vs.ClipSurface(h1, h2)
	h3 = vs.PrevObj(h2)
	if h3 != h1:
		vs.SetFPat(h3, 5)
ClipSurfaceExample()
```

```pascal
ClipSurface(shaftH, holeH);
ClipSurface(baseH, holeH);
DelObject(holeH);

 			theWidth/2,
 			#270,
 			#theAngle);
arc2H := LNewObj;
ClipSurface(arc1H, arc2H);
DelObject(arc2H);
 		NoAngleVar;
 		{ below we use GetXsAndYs to calculate where to draw the end line for the object }
 		GetXsAndYs(radius+theWidth/2,  theAngle, theWidth/2);

BEGIN
boo := GetHole(h, cnt, hole);
hole := CopyPoly(hole,FALSE);
ClipSurface(poly, hole);
poly := PrevObj(hole);
DelObj(hole);
END;
```
```python
import vs

# Creates a new surface object by subtracting the intersection of surfaces s1
# and s2 from s1.
s1 = vs.FSActLayer()  # handle to the first selected object on the active layer
s2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.ClipSurface(s1, s2)
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
