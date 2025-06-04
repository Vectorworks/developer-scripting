# SetVertexVisibility

## Description
Sets the visibility of the specified vertex of the referenced object.

```pascal
PROCEDURE SetVertexVisibility(
				h       : HANDLE;
				vertnum : INTEGER;
				vis     : BOOLEAN);
```

```python
def vs.SetVertexVisibility(h, vertnum, vis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the polygon or polyline.|
|vertnum|INTEGER|Index of the vertex (zero-based).|
|vis|BOOLEAN|Visibility of the vertex.|

## See Also
VS Functions:
[GetVertexVisibility](GetVertexVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
