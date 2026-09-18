# GetTextureRef

## Description
Function GetTextureRef returns the texture reference ID for the referenced object. The integer returned is the internal index of the texture node used by this object.

```pascal
FUNCTION GetTextureRef(
				obj            : HANDLE;
				partID         : INTEGER;
				resolveByClass : BOOLEAN): LONGINT;
```

```python
def vs.GetTextureRef(obj, partID, resolveByClass):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Identifies texture to be returned by part ID.|
|resolveByClass|BOOLEAN|Resolve texture reference by class.|

## Remarks
Returns the texture ref for this object, which is the internal index, or name, of the texture node used by this object.  The texture is specific to the partID part of the object (0 = Primary, 1 = Secondary, or 2 = Tertiary).  Walls can have three different textures and roofs can have two if they are 'expanded'.  Textures may be applied by class.  If resolveByClass is true then this function will return the texture ref for this object?s class.

I'd expected the 'resolveByClass' to be a VAR. Instead you can use GetTextureRef(obj, partID, FALSE). The longint returned will be -1, if the texture is by class:

```pascal
message(GetTextureRef(obj, partID, TRUE), ' * ', GetTextureRef(obj, partID, FALSE));
{ returns the id of the texture on the left call and -1 on the right call, if it is by class }
```

See [SetTextureRef](SetTextureRef.md) remarks.

## Examples
```pascal
IF GetClass(objectHand) = noneClass THEN BEGIN {Only do things in the container class and roof container is skipped.}
	IF (GetTextureSpace(objectHand,0) = NIL)  THEN
		AttachDefaultTextureSpace(objectHand, 0);  {Attach a texture space to the object.}
	PartTexIndex := GetTextureRef(objectHand, 0, FALSE); {Get the texture index assigned to the PIO.}
	IF( (PartTexIndex = -1) OR (PartTexIndex = 0)) THEN
	BEGIN
		IF GetTypeN(objectHand) = 71 THEN SetTextureRef(objectHand, textureIndex, 14);{Set texture to slab top}
		SetTextureRef(objectHand, textureIndex, 0); {Attach the proper texture to the object.}

IF IsTextureableObject(objectHand) THEN BEGIN
	IF GetClass(objectHand) = noneClass THEN BEGIN {Only do things in the container class.}
		IF (GetTextureSpace(objectHand,0) = NIL)  THEN
			AttachDefaultTextureSpace(objectHand, 0);  {Attach a texture space to the object.}
		PartTexIndex := GetTextureRef(objectHand, 0, FALSE); {Get the texture index assigned to the PIO.}
		IF( (PartTexIndex = -1) OR (PartTexIndex = 0)) THEN
		BEGIN
			SetTextureRef(objectHand, PIOTexIndex, 0); {Attach the proper texture to the object.}
		END;

BEGIN
	EndXTrd;
	textureIndex := GetTextureRef(gPluginH, 0, FALSE);
	SetTextureRef(LNewObj, textureIndex, 0);
	IF viewChanged THEN
	BEGIN
		SetView(xAngleR, yAngleR, zAngleR, offsetX, offsetY, offsetZ);
```
```python
import vs

# Function GetTextureRef returns the texture reference ID for the referenced
# object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
resolveByClass = True

resultN = vs.GetTextureRef(obj, partID, resolveByClass)
vs.Message('GetTextureRef returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
