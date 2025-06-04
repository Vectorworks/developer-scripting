# LayerRef

## Description
Procedure LayerRef places a layer reference (layer link) into the active layer at location (0,0).

```pascal
PROCEDURE LayerRef(layerName : STRING);
```

```python
def vs.LayerRef(layerName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|Name of referenced layer.|

## Examples
#### VectorScript ####
```pascal
LayerRef('Layer-2');
{creates a layer link of 'Layer-2' on the active layer}
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Layers](../Categories/Layers.md)
