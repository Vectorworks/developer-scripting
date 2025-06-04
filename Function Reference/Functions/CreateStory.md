# CreateStory

## Description
Creates a Story. Stories are used to group layers and are shown on the Story pane of the Organization dialog.

```pascal
FUNCTION CreateStory(
				name   : STRING;
				suffix : STRING): BOOLEAN;
```

```python
def vs.CreateStory(name, suffix):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the Story to create.|
|suffix|STRING|The suffix to be used at the end of the name of a Layer associated with the Story.|

## Examples
```pascal
VAR

success:BOOLEAN

BEGIN

success := CreateStory('4th Floor', '4');
```

## See Also
VS Functions:
[GetNumStories](GetNumStories.md) 
| [GetStoryOfLayer](GetStoryOfLayer.md) 
| [AssociateLayerWithStory](AssociateLayerWithStory.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
