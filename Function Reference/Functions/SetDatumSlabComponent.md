# SetDatumSlabComponent

## Description
Sets the datum slab component of an object.

```pascal
PROCEDURE SetDatumSlabComponent(
				obj                : HANDLE;
				datumSlabComponent : INTEGER);
```

```python
def vs.SetDatumSlabComponent(obj, datumSlabComponent):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a slab, Slab Style, or the Slab Preferences.|
|datumSlabComponent|INTEGER|The index of the datum slab component.|

## Examples
```pascal
SetDatumSlabComponent(obj, 1);
```
```python
import vs

# Sets the datum slab component of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
datumSlabComponent = 1

vs.SetDatumSlabComponent(obj, datumSlabComponent)
```

## See Also
VS Functions:
[GetDatumSlabComponent](GetDatumSlabComponent.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
