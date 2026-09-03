# Move3DObj

## Description
Procedure Move3DObj moves the referenced object a specified  distance from its current location. Movement distances are calculated from the 3D center of the object.

```pascal
PROCEDURE Move3DObj(
				h         : HANDLE;
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.Move3DObj(h, xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|xDistance|REAL|X offset distance.|
|yDistance|REAL|Y offset distance.|
|zDistance|REAL|Z offset distance.|

## Examples
[Manipulate3DObjects](examples/Manipulate3DObjects.md)

```pascal
	   SET3DRot(LNewObj,0, 90, 0, -LongDoor-SideReveal+ShortDoor,  -gBottomReveal-gDepth-gKickHeight ,0) ;
	IF gDoorConfig = kDoorConfigBiParting  THEN
		SET3DRot(LNewObj,0, -90, 0, -LongDoor-SideReveal, -gBottomReveal-gDepth-gKickHeight, 0) ;
END;
IF NOT bFlush THEN Move3DObj(LNewObj,0,0,gDoorThick);

	FillBack(65535,65535,65535);
	Oval(-(0.35*cWidth),(0.35*cWidth),(0.35*cWidth),-(0.35*cWidth));
EndXtrd;
Rotate3D(xrot,yrot,zrot);
Move3Dobj(lnewobj,xtr,ytr,ztr);
BeginXtrd(6*upi,9*upi);
	FillBack(0,0,0);
	Rect(-1*upi,.35*cWidth-3*upi,1*upi,-3*upi);
EndXtrd;

		Relative;
		Rect (0, 0 , width, -thk);
	EndSweep;
	SET3DRot(LNewObj, 90, 0, 180, 0, 0, 0);
	Move3DObj(LNewObj, radius, 0, 0);
	Absolute;
END; { of spiral3d }
{-------------------------------------------------------------------}
PROCEDURE Arrow;
```
```python
import vs

# Procedure Move3DObj moves the referenced object a specified distance from
# its current location.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
xDistance = 1.0
yDistance = 1.0
zDistance = 1.0

vs.Move3DObj(h, xDistance, yDistance, zDistance)
```
See also in tutorials: [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md)

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
