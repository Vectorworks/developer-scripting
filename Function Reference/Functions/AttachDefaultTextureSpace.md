# AttachDefaultTextureSpace

## Description
Procedure AttachDefaultTextureSpace deletes any pre-existing space attached to the referenced object and creates a new one with the default object texture.

```pascal
PROCEDURE AttachDefaultTextureSpace(
				obj    : HANDLE;
				partID : INTEGER);
```

```python
def vs.AttachDefaultTextureSpace(obj, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
Deletes any pre-existing space attached to the object (with the specified part ID), creates a new one with the default value for this type of object, and attaches the texture space to the object.

## Examples
```pascal
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

AttachDefaultTextureSpace( resultH, 0 );
{ use common stringer class here. }
IF ( gActStringerPane < 2 ) THEN stringerClassStr := gLStringerClassData.strClassActualName
ELSE                             stringerClassStr := gRStringerClassData.strClassActualName;
{by:PP set texture part overall = 3}
```
```python
if ( vs.GetTextureSpace( objectHand, 0 ) == 0 ):
	# Attach a texture space to the object.
	vs.AttachDefaultTextureSpace( objectHand, 0 )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
