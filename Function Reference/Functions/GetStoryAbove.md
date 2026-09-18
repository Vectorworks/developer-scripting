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

```pascal
BEGIN
	storyH := GetStoryAbove( storyH );
END;

{ Find the story we are currently working on }
hStory := GetStoryBelow( NIL );
storySuffix := GetStorySuffix( hStory );
WHILE (( storySuffix  <> TmpLayerSuffix ) AND ( hStory <> NIL ) ) DO BEGIN
	hStory := GetStoryAbove( hStory );
	if ( hStory <> NIL ) THEN BEGIN
		storySuffix := GetStorySuffix( hStory );
	END;

3: BEGIN
	story := GetStoryBelow(NIL);
	WHILE story <> NIL DO BEGIN
		AddChoice(dialogID, 10, GetStorySuffix(story), 0);
		story := GetStoryAbove(story);
	END;
```
```python
import vs

# Returns the Story above the indicated Story.
story = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetStoryAbove(story)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
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
