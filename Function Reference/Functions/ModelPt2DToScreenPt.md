# ModelPt2DToScreenPt

## Description
Transforms a point from world coordinate to the screen coordinates in plan rotation.

```pascal
PROCEDURE ModelPt2DToScreenPt(VAR pX,pY : REAL);
```

```python
def vs.ModelPt2DToScreenPt(p):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Remarks
This routine transform  a given point from model(object) to VCS.

## Examples
```pascal
		locusH := gObjH2;
		objH := gObjH1;
	END;
	GetLocPt (locusH, gXu, gYu);
	ModelPt2DToScreenPt (gXu, gYu);
END	{of anotherAxis}

BEGIN
	HRotate (objH, 0, 0, -gVCSAngle);
	ModelPt2DToScreenPt (xc, yc);
	Locus (xc, yc);
	locusH := LNewObj;
	HRotate (locusH, 0, 0, -gVCSAngle);
	GetLocPt (locusH, xc, yc);

SetCursor(WATCHC);
fPenFore(red,green,blue);
PenFore(65535,0,0);
{** Enter the Grid }
ModelPt2DToScreenPt(x, y);
FOR r := 1 TO numRows DO BEGIN
	curY := y - ((r-1) * gridFreq);
	FOR c := 1 TO numCols DO BEGIN
		curX := x + ((c-1) * gridFreq);
```
```python
import vs

# Transforms a point from world coordinate to the screen coordinates in plan
# rotation.
p = (0, 0)

result = vs.ModelPt2DToScreenPt(p)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
