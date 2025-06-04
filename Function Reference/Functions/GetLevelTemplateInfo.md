# GetLevelTemplateInfo

## Description
Used to access the properties of the Story Level Template at 'index'.  The name, scaleFactor, levelType, elevation, and wallHeight parameters of the requested Story Level Template will be returned in the appropriate parameters.

```pascal
FUNCTION GetLevelTemplateInfo(
				index           : INTEGER;
				VAR layerName   : STRING;
				VAR scaleFactor : REAL;
				VAR levelType   : STRING;
				VAR elevation   : REAL;
				VAR wallHeight  : REAL): BOOLEAN;
```

```python
def vs.GetLevelTemplateInfo(index):
    return (BOOLEAN, layerName, scaleFactor, levelType, elevation, wallHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the desired Story Level Template.|
|layerName|STRING|The layer name associated with the Story Level Template at 'index'.  If this is empty, the corresponding Story Level Template does not use or create a layer.|
|scaleFactor|REAL|The scale of the layer associated with the Story Level Template at 'index'.  If this layer name is blank, this parameter has no use.|
|levelType|STRING|The level type of the Story Level Template at 'index'.|
|elevation|REAL|The elevation of the Story Level Template at 'index'.|
|wallHeight|REAL|The wall height of the Story Level Template at 'index'.  If the layer name is blank, this parameter has no meaning.|

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
