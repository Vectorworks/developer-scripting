# GetLayerTransparency

## Description
Return the tranparency of the current layer.

```pascal
FUNCTION GetLayerTransparency : REAL;
```

```python
def vs.GetLayerTransparency():
    return REAL
```

## Examples
```pascal
resultVal := GetLayerTransparency;
```
```python
import vs

# Return the tranparency of the current layer.
value = vs.GetLayerTransparency()
vs.Message('GetLayerTransparency returned: ' + str(value))
```

## See Also
VS Functions:
[SetLayerTransparency](SetLayerTransparency.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
