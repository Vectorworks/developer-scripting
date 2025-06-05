# Layer

## Description
Procedure Layer creates a new layer in a VectorWorks document. After creation, the new layer becomes the active layer of the document.

Layer can also be used to switch the active layer of the document. If the layer name passed to the procedure already exists, the procedure switches the active layer to the specified layer.

Single quotes should be avoided in layer names, as they will be treated as a mismatched string specifier, and will cause an error to be generated.

```pascal
PROCEDURE Layer(name : STRING);
```

```python
def vs.Layer(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of new or existing layer.|

## Examples
[IsolateLayer](examples/IsolateLayer.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
