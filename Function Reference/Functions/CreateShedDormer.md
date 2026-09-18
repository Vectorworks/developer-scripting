# CreateShedDormer

## Description
Function CreateShedDormer creates a shed dormer in the referenced roof object.

```pascal
FUNCTION CreateShedDormer(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateShedDormer(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Remarks
This only creates the object, SetDormerAttributes() &amp; SetShedAttributes() must still be called to define the attributes of the dormer.

## Examples
[CreateShedDormer](examples/CreateShedDormer.md)

```pascal
resultN := CreateShedDormer(roofObject);
```
```python
import vs

# Function CreateShedDormer creates a shed dormer in the referenced roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.CreateShedDormer(roofObject)
vs.Message('CreateShedDormer returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
