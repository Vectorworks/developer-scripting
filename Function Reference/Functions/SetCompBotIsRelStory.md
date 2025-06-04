# SetCompBotIsRelStory

## Description
Sets whether or not the component bottom is relative to a story.

```pascal
FUNCTION SetCompBotIsRelStory(
				object                  : HANDLE;
				componentIndex          : INTEGER;
				bottomIsRelativeToStory : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompBotIsRelStory(object, componentIndex, bottomIsRelativeToStory):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|bottomIsRelativeToStory|BOOLEAN|Whether or not the component bottom is relative to a story.|

## See Also
VS Functions:
[GetCompBotIsRelStory](GetCompBotIsRelStory.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
