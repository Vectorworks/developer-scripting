# GetDatumSlabComponent

## Description
Gets the datum slab component of an object.

```pascal
FUNCTION GetDatumSlabComponent(obj : HANDLE): INTEGER;
```

```python
def vs.GetDatumSlabComponent(obj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a slab, Slab Style, or the Slab Preferences.|

## Examples
```pascal
resultN := GetDatumSlabComponent(obj);
```
```python
import vs

# Gets the datum slab component of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetDatumSlabComponent(obj)
vs.Message('GetDatumSlabComponent returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetDatumSlabComponent](SetDatumSlabComponent.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
