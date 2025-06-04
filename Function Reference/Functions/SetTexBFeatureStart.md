# SetTexBFeatureStart

## Description
Procedure SetTexBFeatureStart sets the &quot;feature startpoint&quot; of the referenced texture bitmap.  The point is expressed in pixels from the top left corner of the bitmap.

```pascal
PROCEDURE SetTexBFeatureStart(
				textureBitmap : HANDLE;
				featureStartX : INTEGER;
				featureStartY : INTEGER);
```

```python
def vs.SetTexBFeatureStart(textureBitmap, featureStartX, featureStartY):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|featureStartX|INTEGER|X coordinate of feature start point.|
|featureStartY|INTEGER|Y coordinate of feature start point.|

## Remarks
X and y are in paint node pixels from top left

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
