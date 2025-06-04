# GetLevelElevationN

## Description
Gets the elevation of a Story Level, relative to its containing Story. The elevation is in document units.

```pascal
FUNCTION GetLevelElevationN(
				storyHandle : HANDLE;
				levelType   : STRING): REAL;
```

```python
def vs.GetLevelElevationN(storyHandle, levelType):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the Story containing the Story Level we would like to know the elevation of.|
|levelType|STRING|The level type of the Story Level that we would like to know the elevation of.|

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevelN](AddStoryLevelN.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [SetLevelElevationN](SetLevelElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
