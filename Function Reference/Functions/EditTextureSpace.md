# EditTextureSpace

## Description
Function EditTextureSpace edits the mapping of a specified texture space for the referenced object. Calling this function opens the Edit Mapping dialog for textures.

```pascal
FUNCTION EditTextureSpace(
				obj    : HANDLE;
				partID : INTEGER): BOOLEAN;
```

```python
def vs.EditTextureSpace(obj, partID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
Brings up the Edit Mapping dialog for the space attached to the object.  Returns true if the texture space was changed by the dialog.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
