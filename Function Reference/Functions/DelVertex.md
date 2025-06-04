# DelVertex

## Description
Procedure DelVertex deletes a vertex from the referenced object. Parameter vertexNum specifies the vertex to be deleted.

```pascal
PROCEDURE DelVertex(
				objectHd  : HANDLE;
				vertexNum : INTEGER);
```

```python
def vs.DelVertex(objectHd, vertexNum):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to polygon.|
|vertexNum|INTEGER|Index of vertex to be deleted.|

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
