# SetMeshVertex

## Description
Set a mesh vertex.

```pascal
PROCEDURE SetMeshVertex(
				hMesh : HANDLE;
				index : INTEGER;
				pt    : REAL);
```

```python
def vs.SetMeshVertex(hMesh, index, pt):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMesh|HANDLE|Handle to the mesh object.|
|index|INTEGER|The Index of the vertex.|
|pt|REAL|The new vertex coordinates.|

## Examples
```pascal
SetMeshVertex(hMesh, 1, 1.0);
```
```python
import vs

# Set a mesh vertex.
hMesh = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1
pt = 1.0

vs.SetMeshVertex(hMesh, index, pt)
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
