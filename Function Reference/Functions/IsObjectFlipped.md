# IsObjectFlipped

## Description
Function IsObjectFlipped returns the flip orientation of the specified 3D object. The function returns TRUE if the object is currently flipped.  

This function works for sweeps, extrudes, multiple extrudes, symbols, solids, layer references, and plug-in objects.

```pascal
FUNCTION IsObjectFlipped(h : HANDLE): BOOLEAN;
```

```python
def vs.IsObjectFlipped(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns true if the object is currently flipped.  Works for sweeps, extrudes, mextrudes, symbols, solids, layer refs, and plug-in objects

[sd 8/19/98]

## Examples
#### VectorScript ####
```pascal
FUNCTION ObjFlippedInWall(objH, wallH :HANDLE) :BOOLEAN;
BEGIN
ObjFlippedInWall := ((Trunc(GetSymRot(objH)) <> Trunc(HAngle(wallH))) = IsObjectFlipped(objH)); 
END;
```
#### Python ####
```python

```

```pascal
BEGIN
rot := -(rot + 90);
IF pFlip THEN rot := rot+180;
IF IsObjectFlipped(parmHand) THEN tRot := getsymrot(parmHand)-180 ELSE tRot := -getsymrot(parmHand);
Arc(x-1*A*kBubbRad,y+LScale*POffset+2*A*kBubbRad,x+1*A*kBubbRad,y+LScale*POffset,0,360.0);
hBubble := lnewobj;
HRotate(hBubble,x,y,-rot);
HCenter(hBubble,xC,yC);

BuildFullName(GetLocStr(11111, 1), 'UpdateResources.vwx', str0);
{$INCLOOD Common\Data\UpdateResources.vwx}
BSB := CopySymbol(str0,gParmN);
theRot:= GetSymRot(ObjH);
isFlipped:= IsObjectFlipped(ObjH);
GetSymLoc(ObjH, x, y);

IF IsObjectFlipped( gMyHand ) THEN
BEGIN
	Hrotate (gOutlineH , Xtemp, Ytemp , 180);
END;
```
```python
if vs.PHorizontal_Text == True and not vs.IsObjectFlipped( gObjHandle ):
	dTextRotation = -pioRotation
elif vs.PHorizontal_Text == True and vs.IsObjectFlipped( gObjHandle ):
	dTextRotation = pioRotation
elif vs.PHorizontal_Text == True and vs.IsObjectFlipped( gObjHandle ) and pioRotation == -180:
```

## See Also
VS Functions:
[IsFlipped](IsFlipped.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
