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

## Examples
```pascal
resultOK := EditTextureSpace(obj, 1);
```
```python
import vs

# Function EditTextureSpace edits the mapping of a specified texture space
# for the referenced object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1

ok = vs.EditTextureSpace(obj, partID)
if ok:
    vs.Message('EditTextureSpace succeeded')
else:
    vs.Message('EditTextureSpace failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
