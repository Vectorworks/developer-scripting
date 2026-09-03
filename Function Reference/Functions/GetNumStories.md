# GetNumStories

## Description
Returns the number of stories in the file. Stories are used to group layers and are shown on the Story pane of the Organization dialog.

```pascal
FUNCTION GetNumStories : INTEGER;
```

```python
def vs.GetNumStories():
    return INTEGER
```

## Examples
```pascal
resultN := GetNumStories;
```
```python
import vs

# Returns the number of stories in the file.
count = vs.GetNumStories()
vs.Message('GetNumStories returned: ' + str(count))
```

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [GetStoryOfLayer](GetStoryOfLayer.md) 
| [AssociateLayerWithStory](AssociateLayerWithStory.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
