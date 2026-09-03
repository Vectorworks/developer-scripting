# WallFootPrint

## Description
Returns the handle of a polyline representing the footprint of a wall.

```pascal
FUNCTION WallFootPrint(wallHandle : HANDLE): HANDLE;
```

```python
def vs.WallFootPrint(wallHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHandle|HANDLE|Handle to the wall|

## Remarks
\_c\_, (2008.01.07): This actually generates the footprint object in the parent container (active layer or whatever other parent). It doesn't only return a handle.

\_c\_, (2011.01.30): You might need to regen it using [ ResetObject](ResetObject.md) in order to actually see/use it in the drawing. Mind that this object is always a screen plane polyline, unregarded the active plane, and that its vertexes are all hidden.

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetWallFootPrint;
VAR
h1, h2 :HANDLE;
BEGIN
h1 := FSActLayer;
h2 := WallFootPrint(h1);
END;
RUN(GetWallFootPrint);
```
#### Python ####
```python

```

```pascal
BEGIN
	ok := FALSE;
	if ( GetType(h) = 68 ) then BEGIN
		h1 := WallFootPrint(h);
		ok := TRUE;
	END else if (GetType(h) = 71) & (GetObjectVariableInt(h, 172) = 3) then BEGIN
		h1 := HDuplicate(FIn3D(h), 0, 0);
		ok := TRUE;

		CreateArcVertices(cen_pt, Vec2Ang(out_END_pt - cen_pt), -sweepAng, out_radius);
		AddPoint(out_beg_pt.x, out_beg_pt.y);
	EndPoly;
	temp_h := LNewObj;
	h := WallFootPrint(h);
	WallFootPrintRound := AddSurface(h, temp_h);
END;
```
```python
result = vs.WallFootPrint(h)
```

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
