# GetTexBFeatureEnd

## Description
Procedure GetTexBFeatureEnd returns the &quot;feature endpoint&quot; of the referenced texture bitmap.  The point is expressed in pixels from the top left corner of the bitmap.

```pascal
PROCEDURE GetTexBFeatureEnd(
				textureBitmap   : HANDLE;
				VAR featureEndX : INTEGER;
				VAR featureEndY : INTEGER);
```

```python
def vs.GetTexBFeatureEnd(textureBitmap):
    return (featureEndX, featureEndY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureBitmap|HANDLE|Handle to texture bitmap.|
|featureEndX|INTEGER|Returns X coordinate of feature end point.|
|featureEndY|INTEGER|Returns Y coordinate of feature end point.|

## Remarks
X and y are in paint node pixels from top left

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
