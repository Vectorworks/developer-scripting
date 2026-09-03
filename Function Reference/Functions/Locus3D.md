# Locus3D

## Description
Procedure Locus3D creates a new 3D locus in the document at the specified 3D coordinate location.

```pascal
PROCEDURE Locus3D(pX,pY,pZ : REAL);
```

```python
def vs.Locus3D(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|3D coordinates of new locus.|

## Examples
```pascal
IF NOT pCreate_3d THEN Locus3d(0,0,0);

	SetClass(capitalH, gCapitalClass);
IF (shaftH <> NIL) & (gShaftClass <> '') THEN
	SetClass(shaftH, gShaftClass);
BeginGroup;
	Locus3D (0,0,0);
	locusH := LNewObj;
EndGroup;
archGroupH := LNewObj;
IF (archGroupH <> NIL) & (gArchClass <> '') THEN

  Creation of parametric object (Stake in our case) won't create any geometry ...
  ... before the menu command finishes (see how 'gVSIsRunning' works).
  On the other hand, the Z values are yet to be specified (using a dialog) ...
  ... so we need some hint geometry (loci) at the positions where objects will be created. }
Locus3D( modelX, modelY, 0.0 );
```
```python
import vs

# Procedure Locus3D creates a new 3D locus in the document at the specified
# 3D coordinate location.
p = (0, 0)

vs.Locus3D(p)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
