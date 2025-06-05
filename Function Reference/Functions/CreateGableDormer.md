# CreateGableDormer

## Description
Function CreateGableDormer creates a gable dormer in the referenced roof object.

```pascal
FUNCTION CreateGableDormer(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateGableDormer(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Remarks
This only creates the object, SetDormerAttributes() &amp; SetGableAttributes() must still be called to define the attributes of the dormer.

## Examples
[CreateRoofOb](examples/CreateRoofObj.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
