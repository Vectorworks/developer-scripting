# GetTextureSpace

## Description
Function GetTextureSpace returns a handle to the texture space attached to the referenced object(or object part).

```pascal
FUNCTION GetTextureSpace(
				obj    : HANDLE;
				partID : INTEGER): HANDLE;
```

```python
def vs.GetTextureSpace(obj, partID):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
*\_c\_*, (2018.12.29) Don't use this: it works but on walls will remove the mapping, tested on VW 2017, 2018. The new GetTexMapXXX routines accept a direct object handle, without needing the texture space handle.

Returns the texture space attached to this object, with the same part ID as partID.  Walls may have three texture spaces attached to them if they have expanded textures, for example.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example; 
VAR
XAxis, YAxis, ZAxis :REAL; 
hObj :HANDLE; 
BEGIN
hObj := GetTextureSpace(FSActLayer, 0); 
GetTexSpaceOrientU(hObj, XAxis, YAxis, ZAxis); 
Writeln('U', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
GetTexSpaceOrientV(hObj, XAxis, YAxis, ZAxis); 
Writeln('V', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
GetTexSpaceOrientW(hObj, XAxis, YAxis, ZAxis); 
Writeln('W', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
END; 
RUN(Example);
```
#### Python ####
```python
def Example():
	hObj = vs.GetTextureSpace(vs.FSActLayer(), 0)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientU(hObj)
	vs.Message('U', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientV(hObj) 
	vs.Message('V', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientW(hObj)
	vs.Message('W', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)

Example()
```

```pascal
Begin
	SetDefaultTexMap (H);
	SetAttrsByClass(H);
	TextSpaceHand := GetTextureSpace(H,0);
	IF TextSpaceHand <> NIL THEN
	BEGIN
		SetTexSpaceKind(TextSpaceHand,MapType);
		IF GetTypeN( H ) = 84 THEN

IF GetClass(objectHand) = noneClass THEN BEGIN {Only do things in the container class and roof container is skipped.}
	IF (GetTextureSpace(objectHand,0) = NIL)  THEN
		AttachDefaultTextureSpace(objectHand, 0);  {Attach a texture space to the object.}
	PartTexIndex := GetTextureRef(objectHand, 0, FALSE); {Get the texture index assigned to the PIO.}
	IF( (PartTexIndex = -1) OR (PartTexIndex = 0)) THEN
	BEGIN
		IF GetTypeN(objectHand) = 71 THEN SetTextureRef(objectHand, textureIndex, 14);{Set texture to slab top}

BEGIN
	IF IsTextureableObject(objectHand) THEN BEGIN
		IF GetClass(objectHand) = noneClass THEN BEGIN {Only do things in the container class.}
			IF (GetTextureSpace(objectHand,0) = NIL)  THEN
				AttachDefaultTextureSpace(objectHand, 0);  {Attach a texture space to the object.}
			PartTexIndex := GetTextureRef(objectHand, 0, FALSE); {Get the texture index assigned to the PIO.}
			IF( (PartTexIndex = -1) OR (PartTexIndex = 0)) THEN
			BEGIN
				SetTextureRef(objectHand, PIOTexIndex, 0); {Attach the proper texture to the object.}
```
```python
if vs.GetClass( objectHand ) == noneClass:
	if ( vs.GetTextureSpace( objectHand, 0 ) == 0 ):
		# Attach a texture space to the object.
		vs.AttachDefaultTextureSpace( objectHand, 0 )
	# Get the texture index assigned to the PIO.
	partTexIndex = vs.GetTextureRefN( objectHand, 0, 0 False )
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
