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

## Examples
```pascal
resultOK := SetCompTopIsRelStory(object, 1, TRUE);
```
```python
import vs

# Sets whether or not the component top is relative to a story.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
topIsRelativeToStory = True

ok = vs.SetCompTopIsRelStory(object, componentIndex, topIsRelativeToStory)
if ok:
    vs.Message('SetCompTopIsRelStory succeeded')
else:
    vs.Message('SetCompTopIsRelStory failed')
```

## See Also
VS Functions:
[GetCompTopIsRelStory](GetCompTopIsRelStory.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
