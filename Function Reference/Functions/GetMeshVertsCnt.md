# GetMeshVertsCnt

## Description
Returns the number of vertices of the passed mesh handle.

```pascal
FUNCTION GetMeshVertsCnt(hMesh : HANDLE): INTEGER;
```

```python
def vs.GetMeshVertsCnt(hMesh):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMesh|HANDLE|Handle to the mesh object.|

## Examples
```pascal
resultN := GetMeshVertsCnt(hMesh);
```
```python
import vs

# Returns the number of vertices of the passed mesh handle.
hMesh = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetMeshVertsCnt(hMesh)
vs.Message('GetMeshVertsCnt returned: ' + str(resultN))
```

## See Also
VS Functions:
[GetMeshVertsCnt](GetMeshVertsCnt.md) 
| [GetMeshVertex](GetMeshVertex.md) 
| [SetMeshVertex](SetMeshVertex.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
