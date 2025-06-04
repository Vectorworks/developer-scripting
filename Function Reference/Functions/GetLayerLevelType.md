# GetLayerLevelType

## Description
Returns the Layer Level Type of the Layer.

```pascal
FUNCTION GetLayerLevelType(layer : HANDLE): STRING;
```

```python
def vs.GetLayerLevelType(layer):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The Layer whose Layer Level Type is desired.|

## Examples
```pascal
VAR

layerLevelType:STRING;

BEGIN

layerLevelType := GetLayerLevelType(ActLayer);
```

## See Also
VS Functions:
[SetLayerLevelType](SetLayerLevelType.md) 
| [CreateLayerLevelType](CreateLayerLevelType.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
