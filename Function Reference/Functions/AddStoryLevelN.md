# AddStoryLevelN

## Description
Adds a new Story Layer to the Story pointed to by 'storyHandle'.  There must not be another story level in this story that matches 'levelType' or 'elevation', or the function will fail.  If the layer 'layerName' already exists, it will be associated with the new Story Level.

```pascal
FUNCTION AddStoryLevelN(
				storyHandle : HANDLE;
				levelType   : STRING;
				elevation   : REAL;
				layerName   : STRING): BOOLEAN;
```

```python
def vs.AddStoryLevelN(storyHandle, levelType, elevation, layerName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the story that the new level should be added to.|
|levelType|STRING|The level type of the new Story Level.  This cannot be blank.|
|elevation|REAL|The elevation of the new Story Level in the story. The elevation is in document units.|
|layerName|STRING|The name of the layer to associate with the new Story Level.  This is optional.|

## Examples
```python
VAR

storyHandle : HANDLE
success:BOOLEAN

BEGIN

storyHandle := CreateStory('Floor 1', '-1');
success := AddStoryLevelN(storyHandle, 'Finish Floor', 0, 'Floor');
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [SetLevelElevationN](SetLevelElevationN.md) 
| [GetLevelElevationN](GetLevelElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
