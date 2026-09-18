# GroupToMesh

## Description
Converts a group of 3D polygons into a mesh network.

```pascal
FUNCTION GroupToMesh(groupObj : HANDLE): HANDLE;
```

```python
def vs.GroupToMesh(groupObj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|groupObj|HANDLE|Handle to a group containing 3D polygons|

## Examples
```pascal
	PixZ := PixZ+gvpitch;
END;
EndGroup;
DomeGroup := ConvertTo3DPolys (LNewObj);
LEDMesh := GroupToMesh (DomeGroup);
```
```python
import vs

# Converts a group of 3D polygons into a mesh network.
groupObj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GroupToMesh(groupObj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[MeshToGroup](MeshToGroup.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
