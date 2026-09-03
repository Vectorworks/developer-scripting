# SetTexBFeatureEnd

## Description
Procedure SetTexBFeatureEnd sets the &quot;feature endpoint&quot; of the referenced texture bitmap.  Parameters featureEndX and featureEndY specify the end point. The point is expressed in pixels from the top left corner of the bitmap.

```pascal
PROCEDURE SetTexBFeatureEnd(
				textureBitmap : HANDLE;
				featureEndX   : INTEGER;
				featureEndY   : INTEGER);
```

```python
def vs.SetTexBFeatureEnd(textureBitmap, featureEndX, featureEndY):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|featureEndX|INTEGER|X coordinate of feature end point.|
|featureEndY|INTEGER|Y coordinate of feature end point.|

## Remarks
X and y are in paint node pixels from top left

## Examples
```pascal
SetTexBFeatureEnd(textureBitmap, 1, 2);
```
```python
import vs

# Procedure SetTexBFeatureEnd sets the &quot;feature endpoint&quot; of the
# referenced texture bitmap.
textureBitmap = vs.FSActLayer()  # handle to the first selected object on the active layer
featureEndX = 1
featureEndY = 2

vs.SetTexBFeatureEnd(textureBitmap, featureEndX, featureEndY)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
