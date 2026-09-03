# PenSize

## Description
Procedure PenSize sets the active line weight for the document.

```pascal
PROCEDURE PenSize(lw : INTEGER);
```

```python
def vs.PenSize(lw):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|lw|INTEGER|Line weight (in mils). Fourteen (14) mils equals one pixel.|

## Examples
#### VectorScript ####
```pascal
PenSize(28);
```
#### Python ####
```python

```

```pascal
BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);
END;

	LineTo(-7.1875e-1',-1.3333e0');
	LineTo(-8.54167e-1',-1.3333e0');
EndPoly;
BeginXtrd(0e0',1.8125e0');
	PenSize(1);
	Poly(
	-8.54167e-1',-1.04167e-1',
	-8.54167e-1',-1.3333e0',
	-7.1875e-1',-1.3333e0',

savePenPat := FPenPatN;
savePenSize := FPenSize;
FPenFore(saveR, saveG, saveB);
PenPatN(gLeaderType);
PenSize(gLeaderThickness);
GetPenFore(ActiveParmHand, r, g, b);
PenFore(r, g, b);
MoveTo(bubbleIntPt.x, bubbleIntPt.y);
LineTo(shoulderPt.x, shoulderPt.y);
```
```python
if not vs.IsLWByClass( objHand ):
	penSize	= vs.GetLW( objHand )
	vs.PenSize( penSize )

if not vs.PShow_Joints:
	# Lines are drawn later because of joints
	vs.PenSize( 0 )

def DrawGutter( r1, sweep2D, w, gutter, currPenSize ):
	theta = vs.Deg2Rad( sweep2D )
	vs.PenSize( currPenSize )
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
