# GetMeshVertex

## Description
Return the specified vertex of a mesh object.

```pascal
PROCEDURE GetMeshVertex(
				hMesh     : HANDLE;
				index     : INTEGER;
				VAR outPt : REAL);
```

```python
def vs.GetMeshVertex(hMesh, index):
    return outPt
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMesh|HANDLE|Handle to the mesh object.|
|index|INTEGER|The Index of the vertex.|
|outPt|REAL|Output parameter. The 3D coordinates of the vertex.|

## Examples
```pascal
GetMeshVertex(hMesh, 1, 1.0);
```
```python
import vs

# Return the specified vertex of a mesh object.
hMesh = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

result = vs.GetMeshVertex(hMesh, index)
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
