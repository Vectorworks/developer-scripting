# CreateLayerLevelType

## Description
Creates a Layer Level Type.  A Layer can be assigned a Layer Level Type, which defines its location within a Story.

```pascal
FUNCTION CreateLayerLevelType(name : STRING): BOOLEAN;
```

```python
def vs.CreateLayerLevelType(name):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the Layer Level Type to create.|

## Examples
```pascal
resultOK := CreateLayerLevelType('Example');
```
```python
import vs

# Creates a Layer Level Type.
name = 'Example'

ok = vs.CreateLayerLevelType(name)
if ok:
    vs.Message('CreateLayerLevelType succeeded')
else:
    vs.Message('CreateLayerLevelType failed')
```

## See Also
VS Functions:
[GetNumLayerLevelTypes](GetNumLayerLevelTypes.md) 
| [GetLayerLevelType](GetLayerLevelType.md) 
| [SetLayerLevelType](SetLayerLevelType.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
