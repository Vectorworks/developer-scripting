# GetCompBotIsRelStory

## Description
Gets whether or not the component bottom is relative to a story.

```pascal
FUNCTION GetCompBotIsRelStory(
				object                      : HANDLE;
				componentIndex              : INTEGER;
				VAR bottomIsRelativeToStory : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompBotIsRelStory(object, componentIndex):
    return (BOOLEAN, bottomIsRelativeToStory)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|bottomIsRelativeToStory|BOOLEAN|Returns whether or not the component bottom is relative to a story.|

## See Also
VS Functions:
[SetCompBotIsRelStory](SetCompBotIsRelStory.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
