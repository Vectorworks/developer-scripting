# DeleteStoryLayerTemplate

## Description
Deletes the nth Story Layer Template from the current file. For example, if 3 is passed in, it will delete the 3rd Story Layer Template in the file.

```pascal
FUNCTION DeleteStoryLayerTemplate(index : INTEGER): BOOLEAN;
```

```python
def vs.DeleteStoryLayerTemplate(index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Index of the Story Layer Template to delete.|

## Examples
```pascal
VAR

success:BOOLEAN;

BEGIN

success := DeleteStoryTemplate(3);
```

## See Also
VS Functions:
[GetNumStoryLayerTemplates](GetNumStoryLayerTemplates.md) 
| [GetStoryLayerTemplateName](GetStoryLayerTemplateName.md) 
| [CreateStoryLayerTemplate](CreateStoryLayerTemplate.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
