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

```pascal
BEGIN
	storyH := GetStoryBelow( storyH );
END;

{ Find the story we are currently working on }
hStory := GetStoryBelow( NIL );
storySuffix := GetStorySuffix( hStory );
WHILE (( storySuffix  <> TmpLayerSuffix ) AND ( hStory <> NIL ) ) DO BEGIN
	hStory := GetStoryAbove( hStory );
	if ( hStory <> NIL ) THEN BEGIN

3: BEGIN
	story := GetStoryBelow(NIL);
	WHILE story <> NIL DO BEGIN
		AddChoice(dialogID, 10, GetStorySuffix(story), 0);
		story := GetStoryAbove(story);
	END;
```
```python
import vs

# Returns the Story below the indicated Story.
story = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetStoryBelow(story)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
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
