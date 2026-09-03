# SetZVals

## Description
Procedure SetZVals sets the Z (layer base elevation) and delta Z (layer thickness) for the active layer.

```pascal
PROCEDURE SetZVals(
				zDistance      : REAL;
				deltaZDistance : REAL);
```

```python
def vs.SetZVals(zDistance, deltaZDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|zDistance|REAL|Layer base elevation (above document ground plane).|
|deltaZDistance|REAL|Layer thickness.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
baseElevation, thickness :REAL;
BEGIN
Layer('Test Layer');
baseElevation := 1;
thickness := 3;
SetZVals(baseElevation, thickness);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
DoubLines(6*upi);
ResetOrientation3D;
SetZVals(0.0,0.0);
ClearCavities;

SetZVals (zVal, deltaZ); {This used to set the default wall height but does not any more, wall make its own set call now.  Leaving it here in case it does something else.}
IF NOT useStyle THEN
	SetWallWidth (thickness);
nVerts := GetVertNum (polyH);
ALLOCATE polyPt [1..nVerts];

BEGIN
SetZVals(zVal , deltaZVal) ;
SetScale(LScale);
END;
```
```python
	vs.BeginFloor( thickness )
	DrawRoadway( r1, sweep2D, w )
else:
	vs.SetZVals( 0, thickness )
	if drop > 0:
		vs.BeginRoof( 0, 0, w, 0, r1 + w / 2, gutterBottomY, -drop, r1, 2, thickness )
		DrawRoadway( r1, sweep2D, w )
		vs.Move3D( 0, 0, drop )
```

## Version
Availability: from MiniCAD4.0

## Category
* [Layers](../Categories/Layers.md)
