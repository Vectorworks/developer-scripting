# GetStoryElevationN

## Description
Returns the elevaton of the indicated Story. The elevation is in document units.

```pascal
FUNCTION GetStoryElevationN(story : HANDLE): REAL;
```

```python
def vs.GetStoryElevationN(story):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story whose elevation is desired.|

## Examples
```pascal
resultVal := GetStoryElevationN(story);
```
```python
import vs

# Returns the elevaton of the indicated Story.
story = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetStoryElevationN(story)
vs.Message('GetStoryElevationN returned: ' + str(value))
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [SetStoryElevationN](SetStoryElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
