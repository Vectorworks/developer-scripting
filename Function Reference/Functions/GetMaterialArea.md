# GetMaterialArea

## Description
Returns the surface area of the object having the specified material.

```pascal
FUNCTION GetMaterialArea(
				h        : HANDLE;
				material : STRING): REAL;
```

```python
def vs.GetMaterialArea(h, material):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|material|STRING|Name of material.|

## Examples
```pascal
resultVal := GetMaterialArea(h, 'Example');
```
```python
import vs

# Returns the surface area of the object having the specified material.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
material = 'Example'

area = vs.GetMaterialArea(h, material)
vs.Message('GetMaterialArea returned: ' + str(area))
```

## See Also
VS Functions:
[GetMaterialVolume](GetMaterialVolume.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
