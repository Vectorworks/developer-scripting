# GetLayerForStory

## Description
Gets the layer with the story and layer level type specified.

```pascal
FUNCTION GetLayerForStory(
				story     : HANDLE;
				levelType : STRING): HANDLE;
```

```python
def vs.GetLayerForStory(story, levelType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story for which the will be looked up for level types.|
|levelType|STRING|The level type of the story, which associated layer will be returned.|

## Examples
```pascal
VAR

layer:HANDLE;

BEGIN

layer:=GetLayerForStory(story);
```

```pascal
{ Is there a current level type being used }
if ( storyLevel <> '' ) THEN BEGIN
	{ Find a layer with this type for the story }
	if ( hStory <> NIL ) THEN BEGIN
		layerH := GetLayerForStory( hStory, storyLevel );
```
```python
import vs

# Gets the layer with the story and layer level type specified.
story = vs.FSActLayer()  # handle to the first selected object on the active layer
levelType = 'Example'

objHandle = vs.GetLayerForStory(story, levelType)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetStoryOfLayer](GetStoryOfLayer.md) 
| [GetNumStories](GetNumStories.md) 
| [CreateStory](CreateStory.md) 
| [AssociateLayerWithStory](AssociateLayerWithStory.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
