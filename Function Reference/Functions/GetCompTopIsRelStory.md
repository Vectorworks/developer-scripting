# GetCompTopIsRelStory

## Description
Gets whether or not the component top is relative to a story.

```pascal
FUNCTION GetCompTopIsRelStory(
				object                   : HANDLE;
				componentIndex           : INTEGER;
				VAR topIsRelativeToStory : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompTopIsRelStory(object, componentIndex):
    return (BOOLEAN, topIsRelativeToStory)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|topIsRelativeToStory|BOOLEAN|Returns whether or not the component top is relative to a story.|

## See Also
VS Functions:
[SetCompTopIsRelStory](SetCompTopIsRelStory.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
