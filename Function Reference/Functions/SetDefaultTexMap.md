# SetDefaultTexMap

## Description
Set the object to have default texture mapping info. Texture resource being used is set with [SetTextureRef](SetTextureRef.md). Similar to [SetDefaultTextureSpace](SetDefaultTextureSpace.md) except that routine has been superseded in version 2009.

```pascal
PROCEDURE SetDefaultTexMap(h : HANDLE);
```

```python
def vs.SetDefaultTexMap(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
BEGIN
    SetDefaultTexMap (slab_h);
	if openDoor then
		SetTexMapReal (slab_h,3,4, angOpened )
	else
		SetTexMapReal (slab_h,3,4, angClosed);

Begin
	SetDefaultTexMap (H);
	SetAttrsByClass(H);
	TextSpaceHand := GetTextureSpace(H,0);
	IF TextSpaceHand <> NIL THEN
	BEGIN

TexObjHan := GetObject (MyTexName);
SelImageIndx := Name2Index(MyTexName);
ImageTextureSpaceHnd := GetTextureSpace(DummyWholeHandle,kTexturePartID);
IF ImageTextureSpaceHnd = NIL THEN SetDefaultTexMap (DummyWholeHandle);
```
```python
import vs

# Set the object to have default texture mapping info.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetDefaultTexMap(h)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
