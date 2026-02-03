# AddLevelFromTemplate

## Description
Adds a new Story Layer to the Story pointed to by 'storyHandle', using the Story Level Template at 'index' as a template.  The story must not already contain a Story Level with the same level type or elevation as the template.  If the template has a layer name set, a new layer will be created and associated with the new Story Level.

```pascal
FUNCTION AddLevelFromTemplate(
				storyHandle : HANDLE;
				index       : INTEGER): BOOLEAN;
```

```python
def vs.AddLevelFromTemplate(storyHandle, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the Story to add the new Story Level to.|
|index|INTEGER|The index of the Story Level Template to use when creating the Story Level.|

## Examples
```pascal
VAR

storyHandle : HANDLE
success:BOOLEAN

BEGIN

storyHandle := CreateStory('Floor 1', '-1');
success := AddLevelFromTemplate(storyHandle,1);
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevel](AddStoryLevel.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [SetLevelElevation](SetLevelElevation.md) 
| [GetLevelElevation](GetLevelElevation.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
