# CreateHipDormer

## Description
Function CreateHipDormer creates a hip dormer in the referenced roof object.

```pascal
FUNCTION CreateHipDormer(roofObject : HANDLE): INTEGER;
```

```python
def vs.CreateHipDormer(roofObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|

## Remarks
This only creates the object, SetDormerAttributes() &amp; SetHipAttributes() must still be called to define the attributes of the dormer.

object: is the roof object into which to add the dormer.

## Examples
[CreateRoofOb](examples/CreateRoofObj.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
