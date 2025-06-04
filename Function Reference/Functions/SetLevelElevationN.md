# SetLevelElevationN

## Description
Sets the elevation of a Story Level relative to its Story.

```pascal
FUNCTION SetLevelElevationN(
				storyHandle  : HANDLE;
				levelType    : STRING;
				newElevation : REAL): BOOLEAN;
```

```python
def vs.SetLevelElevationN(storyHandle, levelType, newElevation):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the Story with the desired Story Level.|
|levelType|STRING|The level type of the Story Level to change the elevation of.|
|newElevation|REAL|The new elevation for the Story Level. The elevation is in document units.|

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevelN](AddStoryLevelN.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [GetLevelElevationN](GetLevelElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
