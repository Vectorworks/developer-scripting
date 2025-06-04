# AddStoryLevel

## Description
Adds a new Story Layer to the Story pointed to by 'storyHandle'.  There must not be another story level in this story that matches 'levelType' or 'elevation', or the function will fail.  If the layer 'layerName' already exists, it will be associated with the new Story Level.

```pascal
FUNCTION AddStoryLevel(
				storyHandle : HANDLE;
				levelType   : STRING;
				elevation   : REAL;
				layerName   : STRING): BOOLEAN;
```

```python
def vs.AddStoryLevel(storyHandle, levelType, elevation, layerName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|storyHandle|HANDLE|The handle of the story that the new level should be added to.|
|levelType|STRING|The level type of the new Story Level.  This cannot be blank.|
|elevation|REAL|The elevation of the new Story Level in the story.|
|layerName|STRING|The name of the layer to associate with the new Story Level.  This is optional.|

## Examples
```python
VAR

storyHandle : HANDLE
success:BOOLEAN

BEGIN

storyHandle := CreateStory('Floor 1', '-1');
success := AddStoryLevel(storyHandle, 'Finish Floor', 0, 'Floor');
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [AddLevelFromTemplate](AddLevelFromTemplate.md) 
| [RemoveStoryLevel](RemoveStoryLevel.md) 
| [SetLevelElevation](SetLevelElevation.md) 
| [GetLevelElevation](GetLevelElevation.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
