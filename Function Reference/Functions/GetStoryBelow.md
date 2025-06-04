# GetStoryBelow

## Description
Returns the Story below the indicated Story. Returns NULL if there is none. If passed a NULL handle, returns the bottom-most Story in the current drawing.

```pascal
FUNCTION GetStoryBelow(story : HANDLE): HANDLE;
```

```python
def vs.GetStoryBelow(story):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The indicated Story for which the Story below it is desired|

## Examples
```pascal
VAR

baseStory:HANDLE;
storyBelow:HANDLE;

BEGIN

baseStory := GetStoryOfLayer(ActLayer);
storyBelow := StoryBelow(baseStory);
```

## See Also
VS Functions:
[GetStoryAbove](GetStoryAbove.md) 
| [GetNumStories](GetNumStories.md) 
| [GetStoryOfLayer](GetStoryOfLayer.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
