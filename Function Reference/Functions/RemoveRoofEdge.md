# RemoveRoofEdge

## Description
Function RemoveRoofEdge removes the specified roof edge from the referenced roof object.

```pascal
FUNCTION RemoveRoofEdge(
				roofObject : HANDLE;
				index      : INTEGER): BOOLEAN;
```

```python
def vs.RemoveRoofEdge(roofObject, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|index|INTEGER|Index of roof edge to be removed.|

## Examples
```pascal
resultOK := RemoveRoofEdge(roofObject, 1);
```
```python
import vs

# Function RemoveRoofEdge removes the specified roof edge from the referenced
# roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

ok = vs.RemoveRoofEdge(roofObject, index)
if ok:
    vs.Message('RemoveRoofEdge succeeded')
else:
    vs.Message('RemoveRoofEdge failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
