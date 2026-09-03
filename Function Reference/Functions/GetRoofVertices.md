# GetRoofVertices

## Description
Function GetRoofVertices returns the number of roof edges in the referenced roof object.

```pascal
FUNCTION GetRoofVertices(roofObject : HANDLE): INTEGER;
```

```python
def vs.GetRoofVertices(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Examples
```pascal
ALLOCATE spaces[1..space_cnt];
floors[floor_cnt].name := layerName;
spaces[space_cnt].name := 'Roof Space';
spaces[space_cnt].floor := layerName;
for index := 1 to GetRoofVertices(h) do BEGIN
	vertex_cnt := vertex_cnt + 1;
	IF vertex_cnt = vertex_alloc THEN ReAllocate;
	temp2 := GetRoofEdge(h, index, v.pt.x, v.pt.y, v.pt.z, projektion, eaveHeight);
	vertices[vertex_cnt] := v; {storing the slope in the z slot ^}
	floors[floor_cnt].pts[index] := vertex_cnt;
```
```python
import vs

# Function GetRoofVertices returns the number of roof edges in the referenced
# roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetRoofVertices(roofObject)
vs.Message('GetRoofVertices returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
