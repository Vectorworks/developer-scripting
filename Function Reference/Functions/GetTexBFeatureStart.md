# GetTexBFeatureStart

## Description
Procedure GetTexBFeatureStart returns the &quot;feature startpoint&quot; of the referenced texture bitmap.   The point is expressed in pixels from the top left corner of the bitmap.

```pascal
PROCEDURE GetTexBFeatureStart(
				textureBitmap     : HANDLE;
				VAR featureStartX : INTEGER;
				VAR featureStartY : INTEGER);
```

```python
def vs.GetTexBFeatureStart(textureBitmap):
    return (featureStartX, featureStartY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|featureStartX|INTEGER|Returns X coordinate of feature start point.|
|featureStartY|INTEGER|Returns Y coordinate of feature start point.|

## Remarks
X and y are in paint node pixels from top left

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
