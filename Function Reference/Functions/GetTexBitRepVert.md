# GetTexBitRepVert

## Description
Function GetTexBitRepVert returns whether the referenced texture bitmap is set to repeat vertically.

```pascal
FUNCTION GetTexBitRepVert(textureBitmap : HANDLE): BOOLEAN;
```

```python
def vs.GetTexBitRepVert(textureBitmap):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Returns TRUE if this texture bitmap repeats vertically.

## Examples
```pascal
resultOK := GetTexBitRepVert(textureBitmap);
```
```python
import vs

# Function GetTexBitRepVert returns whether the referenced texture bitmap is
# set to repeat vertically.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetTexBitRepVert(textureBitmap)
if ok:
    vs.Message('GetTexBitRepVert succeeded')
else:
    vs.Message('GetTexBitRepVert failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
