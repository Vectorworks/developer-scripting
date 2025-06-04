# SetCompTopIsRelStory

## Description
Sets whether or not the component top is relative to a story.

```pascal
FUNCTION SetCompTopIsRelStory(
				object               : HANDLE;
				componentIndex       : INTEGER;
				topIsRelativeToStory : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompTopIsRelStory(object, componentIndex, topIsRelativeToStory):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|topIsRelativeToStory|BOOLEAN|Whether or not the component top is relative to a story.|

## See Also
VS Functions:
[GetCompTopIsRelStory](GetCompTopIsRelStory.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
