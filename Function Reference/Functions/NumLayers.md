# NumLayers

## Description
Function NumLayers returns the current number of layers within the active document.

```pascal
FUNCTION NumLayers : INTEGER;
```

```python
def vs.NumLayers():
    return INTEGER
```

## Examples
```pascal
resultN := NumLayers;
```
```python
import vs

# Function NumLayers returns the current number of layers within the active
# document.
count = vs.NumLayers()
vs.Message('NumLayers returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
