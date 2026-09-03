# SetTextureSize

## Description
Sets the texture size in real-world inches.

```pascal
PROCEDURE SetTextureSize(
				texture : HANDLE;
				newSize : REAL);
```

```python
def vs.SetTextureSize(texture, newSize):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|texture|HANDLE|   |
|newSize|REAL|   |

## Examples
```pascal
BEGIN
SetName(TextureHand,TextureName);
SetTextureSize(TextureHand, 2");
SetTextureAttributes := TRUE;
END;

If ValidNumStr(Concat(2/GetPrefReal(152),'"'),Size) THEN BEGIN END;
SetTextureSize (BrdrBlckTxtrHnd,Size);
```
```python
import vs

# Sets the texture size in real-world inches.
texture = vs.FSActLayer()  # handle to the first selected object on the active layer
newSize = 1.0

vs.SetTextureSize(texture, newSize)
```

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
