# IsTextureableObject

## Description
Function IsTextureableObject returns whether the referenced object supports texture mapping.

```pascal
FUNCTION IsTextureableObject(obj : HANDLE): BOOLEAN;
```

```python
def vs.IsTextureableObject(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|

## Remarks
This function returns true if the specified 3D object can have textures attached to it.

## Examples
```pascal
BEGIN
	IF IsTextureableObject(hobj) THEN BEGIN
		IF Name2Index(ClassName) = 0 THEN BEGIN
			activeClName:= ActiveClass;
			NameClass(ClassName);
			NameClass(activeClName);
		END;

BEGIN
	IF IsTextureableObject(objectHand) AND NOT(GetTypeN(objectHand) = 83) THEN BEGIN

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
def AssignTex( objectHand ):
	if vs.IsTextureableObject( objectHand ):
		noneClass = vs.GetClass( objectHand )
		# Only do things in the container class.
		if vs.GetClass( objectHand ) == noneClass:
			if ( vs.GetTextureSpace( objectHand, 0 ) == 0 ):
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
