# RemoveStoryLevel

## Description
Removes the Story Level matching 'levelType'  from a Story.  If 'bDeleteLayer' is true and the Story Level has an associated layer, the layer will be deleted as well.

```pascal
FUNCTION RemoveStoryLevel(
				storyHandle  : HANDLE;
				levelType    : STRING;
				bDeleteLayer : BOOLEAN): BOOLEAN;
```

```python
def vs.RemoveStoryLevel(storyHandle, levelType, bDeleteLayer):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the story we want to deleted a Story Level from.|
|levelType|STRING|The level type of the Story Level we want to remove from 'storyHandle'.|
|bDeleteLayer|BOOLEAN|If this is true, and the requested Story Level has a layer associated with it, the layer will be deleted as well.|

## Examples
```pascal
VAR

storyHandle : HANDLE
success:BOOLEAN

BEGIN

storyHandle := CreateStory('Floor 1', '-1');
success := RemoveStoryLevel(storyHandle, 'Finish Floor', TRUE);
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevel](AddStoryLevel.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [SetLevelElevation](SetLevelElevation.md) 
| [GetLevelElevation](GetLevelElevation.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
