# GetLevelTemplateName

## Description
Returns the name of the nth Story Level Template in the file. For example, if 3 is passed in, it will return the name of the 3rd Story Level Template in the file.

```pascal
FUNCTION GetLevelTemplateName(index : INTEGER): STRING;
```

```python
def vs.GetLevelTemplateName(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the Story Level Template whose name is to be returned.|

## Examples
```python
VAR

templateName:STRING;

BEGIN

templateName:=GetLevelTemplateName(2);
```

## See Also
VS Functions:
[GetNumLevelTemplates](GetNumLevelTemplates.md) 
| [SetLevelTemplateName](SetLevelTemplateName.md) 
| [CreateLevelTemplate](CreateLevelTemplate.md) 
| [DeleteLevelTemplate](DeleteLevelTemplate.md) 
| [GetLevelTemplateInfo](GetLevelTemplateInfo.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
