# GetStoryOfLayer

## Description
Returns the Story that the indicated Layer is associated with. Returns NULL if the Layer is not associated with a Story.

```pascal
FUNCTION GetStoryOfLayer(layer : HANDLE): HANDLE;
```

```python
def vs.GetStoryOfLayer(layer):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The Layer for which the associated Story is returned.|

## Examples
```pascal
VAR

story:HANDLE;

BEGIN

story:=GetStoryOfLayer(ActLayer);
```

## See Also
VS Functions:
[GetLayerForStory](GetLayerForStory.md) 
| [GetNumStories](GetNumStories.md) 
| [CreateStory](CreateStory.md) 
| [AssociateLayerWithStory](AssociateLayerWithStory.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
