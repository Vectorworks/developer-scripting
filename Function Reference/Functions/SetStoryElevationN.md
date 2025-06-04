# SetStoryElevationN

## Description
Sets the elevation of the indicated Story. Returns whether the elevation was successfully set. If the elevaton change would cause Layers associated with the Story to overlap Layers associated with another Story, then the change in elevation will be prevented.

```pascal
FUNCTION SetStoryElevationN(
				story     : HANDLE;
				elevation : REAL): BOOLEAN;
```

```python
def vs.SetStoryElevationN(story, elevation):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story whose elevation is to be set.|
|elevation|REAL|The elevation to set the Story to. The elevation is in document units.|

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [GetStoryElevationN](GetStoryElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
