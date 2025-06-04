# GrayLayer

## Description
Procedure GrayLayer sets the visibility status of the active layer to grayed. Objects on grayed layers will always appear grayed when viewed from other layers.

```pascal
PROCEDURE GrayLayer;
```

```python
def vs.GrayLayer():
    return None
```

## Examples
#### VectorScript ####
```pascal
Layer('Future Construction');
GrayLayer;
{grays the layer 'Future Construction'}
```
#### Python ####
```python
vs.Layer('Future Construction')
vs.GrayLayer()
#{grays the layer 'Future Construction'}
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
