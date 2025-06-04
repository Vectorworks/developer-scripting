# CreateLevelTemplateN

## Description
Creates a Story Level Template in the current file. Sets the index parameter to the index of the new template in the list of templates. Story Levels contain a level type, elevation, and optional layer to be used to bound objects on stories; Story Level Templates define a generic level that can be added to multiple stories.

```pascal
FUNCTION CreateLevelTemplateN(
				layerName   : STRING;
				scaleFactor : REAL;
				levelType   : STRING;
				elevation   : REAL;
				wallHeight  : REAL;
				VAR index   : INTEGER): BOOLEAN;
```

```python
def vs.CreateLevelTemplateN(layerName, scaleFactor, levelType, elevation, wallHeight):
    return (BOOLEAN, index)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|The layer name for the new Story Level Template.  This can be blank, meaning that layers will not be created for instances of the new Story Level Template.|
|scaleFactor|REAL|The scale factor for the (optional) layer associated with this Story Level Template.|
|levelType|STRING|The level type for the new Story Level Template.  There may be multiple Story Level Templates with the same level type, as long as they have different elevations.|
|elevation|REAL|The elevation of the Story Level Template, relative to the height of the story in which the level is used. The elevation is in document units.|
|wallHeight|REAL|The wall height for (optional) layers created when using this Story Level Template in a Story. The wall height is in document units. If the layer name is empty, this parameter is unused.|
|index|INTEGER|After the function is called, this parameter contains the index of the new Story Level Template.|

## Examples
```python
VAR

success:BOOLEAN;
index:INTEGER;

BEGIN

success := CreateLevelTemplateN('Mod-Slab', 1, 'LT_Slab', 0, 6, index);
```

## See Also
VS Functions:
[GetNumLevelTemplates](GetNumLevelTemplates.md) 
| [GetLevelTemplateName](GetLevelTemplateName.md) 
| [SetLevelTemplateName](SetLevelTemplateName.md) 
| [DeleteLevelTemplate](DeleteLevelTemplate.md) 
| [GetLevelTemplateInfoN](GetLevelTemplateInfoN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
