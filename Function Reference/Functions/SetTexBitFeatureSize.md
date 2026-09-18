# SetTexBitFeatureSize

## Description
Procedure SetTexBitFeatureSize sets the feature size of the referenced bitmap. Parameter featureSize specifies the size in real world inches.

```pascal
PROCEDURE SetTexBitFeatureSize(
				textureBitmap : HANDLE;
				featureSize   : REAL);
```

```python
def vs.SetTexBitFeatureSize(textureBitmap, featureSize):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|featureSize|REAL|Feature size value.|

## Remarks
featureSize is in real-world inches

## Examples
```pascal
SetTexBitFeatureSize(textureBitmap, 1.0);
```
```python
import vs

# Procedure SetTexBitFeatureSize sets the feature size of the referenced bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer
featureSize = 1.0

vs.SetTexBitFeatureSize(textureBitmap, featureSize)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
