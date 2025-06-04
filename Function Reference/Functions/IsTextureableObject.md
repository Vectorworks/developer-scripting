# IsTextureableObject

## Description
Function IsTextureableObject returns whether the referenced object supports texture mapping.

```pascal
FUNCTION IsTextureableObject(obj : HANDLE): BOOLEAN;
```

```python
def vs.IsTextureableObject(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|

## Remarks
This function returns true if the specified 3D object can have textures attached to it.

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
