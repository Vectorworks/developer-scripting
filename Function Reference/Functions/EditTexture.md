# EditTexture

## Description
Function EditTexture opens the Edit Texture dialog for the referenced texture.

```pascal
FUNCTION EditTexture(texture : HANDLE): BOOLEAN;
```

```python
def vs.EditTexture(texture):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|Handle to texture.|

## Remarks
Brings up the Edit Texture dialog for this texture

## Examples
```pascal
BEGIN
BackUpTextureName := TextureName;
DidIt := SetTextureAttributes;
IF DidIt THEN
	EditTextureDialog := EditTexture(TextureHand)
ELSE
	DelObject(TextureHand);
END;
```
```python
import vs

# Function EditTexture opens the Edit Texture dialog for the referenced texture.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.EditTexture(texture)
if ok:
    vs.Message('EditTexture succeeded')
else:
    vs.Message('EditTexture failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
