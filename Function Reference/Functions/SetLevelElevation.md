# SetLevelElevation

## Description
Sets the elevation of a Story Level relative to its Story.

```pascal
FUNCTION SetLevelElevation(
				storyHandle  : HANDLE;
				levelType    : STRING;
				newElevation : REAL): BOOLEAN;
```

```python
def vs.SetLevelElevation(storyHandle, levelType, newElevation):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the Story with the desired Story Level.|
|levelType|STRING|The level type of the Story Level to change the elevation of.|
|newElevation|REAL|The new elevation for the Story Level.|

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevel](AddStoryLevel.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [GetLevelElevation](GetLevelElevation.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
