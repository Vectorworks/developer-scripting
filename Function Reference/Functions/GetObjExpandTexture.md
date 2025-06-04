# GetObjExpandTexture

## Description
Function GetObjExpandTexture returns whether the referenced objects' textures have been &quot;expanded&quot;. When a texture is expanded, different components of an object can have different textures.

```pascal
FUNCTION GetObjExpandTexture(obj : HANDLE): BOOLEAN;
```

```python
def vs.GetObjExpandTexture(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|

## Remarks
This function returns true if the object's textures are expanded.  For example, if the object is a wall and this function returns true then there are three distinct textures applied to the left, center, and right polygons.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
