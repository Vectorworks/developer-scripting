# GetMaterialVolume

## Description
Returns the volume of the object having the specified material.

```pascal
FUNCTION GetMaterialVolume(
				h        : HANDLE;
				material : STRING): REAL;
```

```python
def vs.GetMaterialVolume(h, material):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object.|
|material|STRING|Name of material.|

## Examples
```pascal
resultVal := GetMaterialVolume(h, 'Example');
```
```python
import vs

# Returns the volume of the object having the specified material.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
material = 'Example'

vol = vs.GetMaterialVolume(h, material)
vs.Message('GetMaterialVolume returned: ' + str(vol))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
