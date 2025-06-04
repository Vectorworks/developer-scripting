# GetStoryLayerTemplateName

## Description
Returns the name of the nth Story Layer Template in the file. For example, if 3 is passed in, it will return the name of the 3rd Story Layer Template in the file.

```pascal
FUNCTION GetStoryLayerTemplateName(index : INTEGER): STRING;
```

```python
def vs.GetStoryLayerTemplateName(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the Story Layer Template whose name is desired.|

## Examples
```pascal
VAR

templateName:STRING;

BEGIN

templateName:=GetStoryLayerTemplateName(2);
```

## See Also
VS Functions:
[GetNumStoryLayerTemplates](GetNumStoryLayerTemplates.md) 
| [CreateStoryLayerTemplate](CreateStoryLayerTemplate.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
