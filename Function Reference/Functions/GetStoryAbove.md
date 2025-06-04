# GetStoryAbove

## Description
Returns the Story above the indicated Story. Returns NULL if there is none. If passed a NULL handle, returns the top-most Story in the current drawing.

```pascal
FUNCTION GetStoryAbove(story : HANDLE): HANDLE;
```

```python
def vs.GetStoryAbove(story):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The indicated Story for which the Story above it is desired.|

## Examples
```pascal
VAR

baseStory:HANDLE;
storyAbove:HANDLE;

BEGIN

baseStory := GetStoryOfLayer(ActLayer);
storyAbove := StoryAbove(baseStory);
```

## See Also
VS Functions:
[GetStoryBelow](GetStoryBelow.md) 
| [GetNumStories](GetNumStories.md) 
| [GetStoryOfLayer](GetStoryOfLayer.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
