# GetPolylineArcMaxRadius

## Description
Return a maximum radius of the specified vertex of type arc or radius of a polyline. <BR>

```pascal
FUNCTION GetPolylineArcMaxRadius(
				hPoly     : HANDLE;
				vertexNum : INTEGER): REAL;
```

```python
def vs.GetPolylineArcMaxRadius(hPoly, vertexNum):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPoly|HANDLE|Handle of the poliline|
|vertexNum|INTEGER|Index of vertex to be queried.|

## Examples
```pascal
resultVal := GetPolylineArcMaxRadius(hPoly, 1);
```
```python
import vs

# Return a maximum radius of the specified vertex of type arc or radius of a
# polyline.
hPoly = vs.FSActLayer()  # handle to the first selected object on the active layer
vertexNum = 1

value = vs.GetPolylineArcMaxRadius(hPoly, vertexNum)
vs.Message('GetPolylineArcMaxRadius returned: ' + str(value))
```

## See Also
VS Functions:
[GetPolylineVertex](GetPolylineVertex.md) 
| [SetPolylineVertex](SetPolylineVertex.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
