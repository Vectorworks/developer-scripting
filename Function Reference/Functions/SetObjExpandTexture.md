# SetObjExpandTexture

## Description
Procedure SetObjExpandTexture sets the &quot;expanded&quot; state of the referenced objects' texture. When a texture is expanded, different components of an object can have different textures.

```pascal
PROCEDURE SetObjExpandTexture(
				obj      : HANDLE;
				expanded : BOOLEAN);
```

```python
def vs.SetObjExpandTexture(obj, expanded):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|expanded|BOOLEAN|Use expanded textures setting.|

## Remarks
Sets whether three or just a single texture is applied to this object (can be up to three for walls or two for roofs).

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
