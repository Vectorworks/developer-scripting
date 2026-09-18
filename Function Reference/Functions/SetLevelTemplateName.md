# SetLevelTemplateName

## Description
Sets the name of the Story Level Template at 'index' to be 'name'.

```pascal
FUNCTION SetLevelTemplateName(
				index : INTEGER;
				name  : STRING): BOOLEAN;
```

```python
def vs.SetLevelTemplateName(index, name):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the Story Level Template.|
|name|STRING|The new name for the Story Level Template at 'index'.|

## Examples
```pascal
VAR

result : BOOLEAN;

BEGIN

result := SetLevelTemplateName(2, &quot;Subfloor&quot;);
```

```pascal
resultOK := SetLevelTemplateName(1, 'Example');
```
```python
import vs

# Sets the name of the Story Level Template at 'index' to be 'name'.
index = 1
name = 'Example'

ok = vs.SetLevelTemplateName(index, name)
if ok:
    vs.Message('SetLevelTemplateName succeeded')
else:
    vs.Message('SetLevelTemplateName failed')
```

## See Also
VS Functions:
[GetNumLevelTemplates](GetNumLevelTemplates.md) 
| [GetLevelTemplateName](GetLevelTemplateName.md) 
| [SetLevelTemplateName](SetLevelTemplateName.md) 
| [CreateLevelTemplate](CreateLevelTemplate.md) 
| [DeleteLevelTemplate](DeleteLevelTemplate.md) 
| [GetLevelTemplateInfo](GetLevelTemplateInfo.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
