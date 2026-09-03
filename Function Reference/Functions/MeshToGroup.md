# MeshToGroup

## Description
Converts meshObj to a group of 3D polygons.

```pascal
FUNCTION MeshToGroup(meshObj : HANDLE): HANDLE;
```

```python
def vs.MeshToGroup(meshObj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|meshObj|HANDLE|Handle to a mesh object|

## Examples
```pascal
resultH := MeshToGroup(meshObj);
```
```python
import vs

# Converts meshObj to a group of 3D polygons.
meshObj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.MeshToGroup(meshObj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GroupToMesh](GroupToMesh.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
