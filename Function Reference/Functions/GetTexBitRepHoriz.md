# GetTexBitRepHoriz

## Description
Function GetTexBitRepHoriz returns whether the referenced texture bitmap is set to repeat horizontally.

```pascal
FUNCTION GetTexBitRepHoriz(textureBitmap : HANDLE): BOOLEAN;
```

```python
def vs.GetTexBitRepHoriz(textureBitmap):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Returns TRUE if this texture bitmap repeats horizontally.

## Examples
```pascal
resultOK := GetTexBitRepHoriz(textureBitmap);
```
```python
import vs

# Function GetTexBitRepHoriz returns whether the referenced texture bitmap is
# set to repeat horizontally.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetTexBitRepHoriz(textureBitmap)
if ok:
    vs.Message('GetTexBitRepHoriz succeeded')
else:
    vs.Message('GetTexBitRepHoriz failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
