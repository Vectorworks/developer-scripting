# CreateBatDormer

## Description
Function CreateBatDormer creates a bat dormer in the referenced roof object.

```pascal
FUNCTION CreateBatDormer(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateBatDormer(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Remarks
This only creates the object, SetDormerAttributes() &amp; SetBatAttributes() must still be called to define the attributes of the dormer.

## Examples
[CreateRoofOb](examples/CreateRoofObj.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
