# UpdateThumbnailPreview

## Description
For a given VectorWorks resource (i.e. Hatch, Texture, Symbol/PIO, etc...), this function will create or update it?s thumbnail preview.

```pascal
FUNCTION UpdateThumbnailPreview(resourceHandle : HANDLE): BOOLEAN;
```

```python
def vs.UpdateThumbnailPreview(resourceHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|resourceHandle|HANDLE|Handle to the resource.|

## Examples
```pascal
GetItemText(dialogID, 4,TextureName );
IF ((TextureName = '') | (BackUpTextureName <> TextureName)) THEN
	IF VerifyName THEN
		DidIt := SetTextureAttributes;
	IF DidIt THEN DidIt := UpdateThumbnailPreview(TextureHand);
END;
```
```python
import vs

# e.
resourceHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.UpdateThumbnailPreview(resourceHandle)
if ok:
    vs.Message('UpdateThumbnailPreview succeeded')
else:
    vs.Message('UpdateThumbnailPreview failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
