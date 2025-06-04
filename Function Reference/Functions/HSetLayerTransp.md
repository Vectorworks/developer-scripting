# HSetLayerTransp

## Description
Set the transparency of the specified layer.

```pascal
PROCEDURE HSetLayerTransp(
				hLayer       : HANDLE;
				transparency : REAL);
```

```python
def vs.HSetLayerTransp(hLayer, transparency):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|Handle to the layer.|
|transparency|REAL|The transparency for the layer. Value between 0.0 and 100.0|

## See Also
VS Functions:
[SetLayerTransparency](SetLayerTransparency.md) 
| [HGetLayerTransp](HGetLayerTransp.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
