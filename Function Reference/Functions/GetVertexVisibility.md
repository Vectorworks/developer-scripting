# GetVertexVisibility

## Description
Returns the visibility of the specified vertex of the referenced object.

```pascal
FUNCTION GetVertexVisibility(
				h       : HANDLE;
				vertnum : INTEGER): BOOLEAN;
```

```python
def vs.GetVertexVisibility(h, vertnum):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the polygon or polyline|
|vertnum|INTEGER|Index of the vertex (zero-based).|

## See Also
VS Functions:
[SetVertexVisibility](SetVertexVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
