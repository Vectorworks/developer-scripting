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

## See Also
VS Functions:
[GetMeshVertsCnt](GetMeshVertsCnt.md) 
| [GetMeshVertex](GetMeshVertex.md) 
| [SetMeshVertex](SetMeshVertex.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
