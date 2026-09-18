# GetLevelElevation

## Description
Gets the elevation of a Story Level, relative to its containing Story.

```pascal
FUNCTION GetLevelElevation(
				storyHandle : HANDLE;
				levelType   : STRING): REAL;
```

```python
def vs.GetLevelElevation(storyHandle, levelType):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the Story containing the Story Level we would like to know the elevation of.|
|levelType|STRING|The level type of the Story Level that we would like to know the elevation of.|

## Examples
```pascal
resultVal := GetLevelElevation(storyHandle, 'Example');
```
```python
import vs

# Gets the elevation of a Story Level, relative to its containing Story.
storyHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
levelType = 'Example'

value = vs.GetLevelElevation(storyHandle, levelType)
vs.Message('GetLevelElevation returned: ' + str(value))
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddStoryLevel](AddStoryLevel.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [SetLevelElevation](SetLevelElevation.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
