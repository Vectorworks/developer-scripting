# GetStoryElevation

## Description
Returns the elevaton of the indicated Story.

```pascal
FUNCTION GetStoryElevation(story : HANDLE): REAL;
```

```python
def vs.GetStoryElevation(story):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story whose elevation is desired.|

## Examples
```pascal
resultVal := GetStoryElevation(story);
```
```python
import vs

# Returns the elevaton of the indicated Story.
story = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetStoryElevation(story)
vs.Message('GetStoryElevation returned: ' + str(value))
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [SetStoryElevation](SetStoryElevation.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
