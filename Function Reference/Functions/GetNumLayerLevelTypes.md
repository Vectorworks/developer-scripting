# GetNumLayerLevelTypes

## Description
Returns the number of layer level types in the file. A layer can be assigned a layer level type, which defines its location within a story.

```pascal
FUNCTION GetNumLayerLevelTypes : INTEGER;
```

```python
def vs.GetNumLayerLevelTypes():
    return INTEGER
```

## Examples
```pascal
resultN := GetNumLayerLevelTypes;
```
```python
import vs

# Returns the number of layer level types in the file.
count = vs.GetNumLayerLevelTypes()
vs.Message('GetNumLayerLevelTypes returned: ' + str(count))
```

## See Also
VS Functions:
[GetLayerLevelType](GetLayerLevelType.md) 
| [SetLayerLevelType](SetLayerLevelType.md) 
| [CreateLayerLevelType](CreateLayerLevelType.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
