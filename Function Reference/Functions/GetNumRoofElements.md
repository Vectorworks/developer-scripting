# GetNumRoofElements

## Description
Function GetNumRoofElements returns the number of roof elements (dormers and skylights) in the referenced roof object.

```pascal
FUNCTION GetNumRoofElements(roofObject : HANDLE): INTEGER;
```

```python
def vs.GetNumRoofElements(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Examples
```pascal
resultN := GetNumRoofElements(roofObject);
```
```python
import vs

# Function GetNumRoofElements returns the number of roof elements (dormers
# and skylights) in the referenced roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetNumRoofElements(roofObject)
vs.Message('GetNumRoofElements returned: ' + str(count))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
