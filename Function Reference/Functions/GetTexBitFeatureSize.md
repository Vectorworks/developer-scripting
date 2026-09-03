# GetTexBitFeatureSize

## Description
Function GetTexBitFeatureSize returns the feature size of the referenced bitmap in real world inches.

```pascal
FUNCTION GetTexBitFeatureSize(textureBitmap : HANDLE): REAL;
```

```python
def vs.GetTexBitFeatureSize(textureBitmap):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|

## Remarks
Returns feature size in real-world inches

## Examples
```pascal
resultVal := GetTexBitFeatureSize(textureBitmap);
```
```python
import vs

# Function GetTexBitFeatureSize returns the feature size of the referenced
# bitmap in real world inches.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetTexBitFeatureSize(textureBitmap)
vs.Message('GetTexBitFeatureSize returned: ' + str(value))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
