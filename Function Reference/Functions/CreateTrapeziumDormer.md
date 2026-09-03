# CreateTrapeziumDormer

## Description
Function CreateTrapeziumDormer creates a trapezium dormer in the referenced roof object.

```pascal
FUNCTION CreateTrapeziumDormer(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateTrapeziumDormer(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Remarks
This only creates the object, SetDormerAttributes() &amp; SetTrapeziumAttributes() must still be called to define the attributes of the dormer.

## Examples
[CreateRoofObj](examples/CreateRoofObj.md)

```pascal
resultN := CreateTrapeziumDormer(roofObject);
```
```python
import vs

# Function CreateTrapeziumDormer creates a trapezium dormer in the referenced
# roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.CreateTrapeziumDormer(roofObject)
vs.Message('CreateTrapeziumDormer returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
