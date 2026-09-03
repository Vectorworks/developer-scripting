# CreateSkylight

## Description
Function CreateSkylight creates a new skylight in the referenced roof object.

```pascal
FUNCTION CreateSkylight(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateSkylight(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Examples
[CreateRoofObj](examples/CreateRoofObj.md)

```pascal
resultN := CreateSkylight(roofObject);
```
```python
import vs

# Function CreateSkylight creates a new skylight in the referenced roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.CreateSkylight(roofObject)
vs.Message('CreateSkylight returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
