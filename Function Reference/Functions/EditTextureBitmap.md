# EditTextureBitmap

## Description
Function EditTextureBitmap opens the Edit Texture Bitmap dialog box to the referenced texture bitmap.  The function returns TRUE if texture bitmap was modified.

```pascal
FUNCTION EditTextureBitmap(textureBitmap : HANDLE): BOOLEAN;
```

```python
def vs.EditTextureBitmap(textureBitmap):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Brings up the Edit Texture Bitmap dialog for this texture bitmap.  Returns true if texture bitmap was changed by the dialog.

## Version
EditTextureBitmap is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
