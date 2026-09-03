# BeginXtrd

## Description
Procedure BeginXtrd creates a 3D extrude object in a VectorWorks document. BeginXtrd uses 2D object creation procedure calls to define the &quot;template&quot; for the object. 

You should call EndXtrd after the object creation procedures to complete the definition and generate the extrude object in the document.

```pascal
PROCEDURE BeginXtrd(
				startDistance : REAL;
				endDistance   : REAL);
```

```python
def vs.BeginXtrd(startDistance, endDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|startDistance|REAL|Start distance from document ground plane.|
|endDistance|REAL|End distance from document ground plane.|

## Examples
[BeginXtrd](examples/BeginXtrd.md)

Another example which will be handy for creating hybrid objects from within plug-ins:
```pascal
{ ***************************************** }
{ Orso.B.Schmid, creates an extrude from a HANDLE h,
  preserving the original h. Returns a handle to the extrude }
FUNCTION Create3Dobj(h: HANDLE; z, dZ: REAL): HANDLE;
BEGIN
  IF h <> NIL THEN BEGIN
    BeginXtrd(z, dZ);
      LineTo(1, 1); { just draw something for creating an extrude container }
    EndXtrd;

    DelObject(FIn3D(GetParent(CreateDuplicateObject(h, LNewObj))));
    { places a copy of h in the extrude and deletes the line }

    Create3Dobj := LNewObj;
  END;
END;
```
#### Python ####
```python

```

```pascal
BEGIN
	BeginXtrd(Bottom,Top);
		ClosePoly;
		Poly(X,Y,-Length-LeftLength,Y,-Length-LeftLength,-Depth+KickInset,-Depth+KickInset,-Length-RightLength,X,-Length-RightLength);
	EndXtrd;
END;

BEGIN
BeginXtrd(Z,CabHeight);
	Poly(X-CabThick, Y-CabThick,
	X-LeftCabLength+CabThick, Y-CabThick,
	X-LeftCabLength+CabThick, Y-CabDepth+FaceThick,
	X-CabDepth+FaceThick, Y-CabDepth+FaceThick,

BeginXtrd(cHeight,cHeight+cRoof_Thickness);
	Rect(-(cWidth/2+cOverhang),-(cWidth/2+cOverhang),(cWidth/2+cOverhang),(cWidth/2+cOverhang));
EndXtrd;
SetTextureRef(lNewObj,-1,3);
```
```python
# Draw 3D gutter
vs.BeginXtrd( 0, thickness )
DrawGutter( r1, sweep2D, w, gutter, currPenSize)
vs.EndXtrd()
SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gPaving_Class )
```
See also in tutorials: [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md)

## See Also
[EndXtrd](EndXtrd.md)

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
