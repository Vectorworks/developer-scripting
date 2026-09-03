# SetDefStoryLayerName

## Description
Sets the name of the nth Default Story Layer in the file. For example, if 3 is passed in, it will set the name of the 3rd Default Story Layer in the file.

```pascal
FUNCTION SetDefStoryLayerName(
				index : INTEGER;
				name  : STRING): BOOLEAN;
```

```python
def vs.SetDefStoryLayerName(index, name):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the default story layer whose name should be set.|
|name|STRING|The name that the indicated default story layer should be set to.|

## Examples
```pascal
VAR

result : BOOLEAN;

BEGIN

result := SetStoryLayerTemplateName(2, &quot;Subfloor&quot;);
```

```pascal
resultOK := SetDefStoryLayerName(1, 'Example');
```
```python
import vs

# Sets the name of the nth Default Story Layer in the file.
index = 1
name = 'Example'

ok = vs.SetDefStoryLayerName(index, name)
if ok:
    vs.Message('SetDefStoryLayerName succeeded')
else:
    vs.Message('SetDefStoryLayerName failed')
```

## See Also
VS Functions:
[GetNumStoryLayerTemplates](GetNumStoryLayerTemplates.md) 
| [GetStoryLayerTemplateName](GetStoryLayerTemplateName.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Layers](../Categories/Layers.md)
