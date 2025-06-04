# HideLayer

## Description
Procedure HideLayer sets the visibility status of the active layer to hidden. Objects on hidden layers will not be viewable from other layers.

```pascal
PROCEDURE HideLayer;
```

```python
def vs.HideLayer():
    return None
```

## Examples
#### VectorScript ####
```pascal
Layer('Future Construction');
HideLayer;
{hides the layer 'Future Construction'}
```
#### Python ####
```python
vs.Layer('Future Construction')
vs.HideLayer()
#{hides the layer 'Future Construction'}
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
