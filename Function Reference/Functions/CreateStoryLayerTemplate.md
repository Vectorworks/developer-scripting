# CreateStoryLayerTemplate

## Description
Creates a Story Layer Template in the current file. Sets the index parameter to the index of the new template in the list of templates. Story Layer Templates are used to define what Layers are typically found in a Story. When a Story is created, the user has the option to automatically create the Layers defined by the Story Layer Templates.

```pascal
FUNCTION CreateStoryLayerTemplate(
				name              : STRING;
				scaleFactor       : REAL;
				layerLevelType    : STRING;
				elevationOffset   : REAL;
				defaultWallHeight : REAL;
				VAR index         : INTEGER): BOOLEAN;
```

```python
def vs.CreateStoryLayerTemplate(name, scaleFactor, layerLevelType, elevationOffset, defaultWallHeight):
    return (BOOLEAN, index)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|The name of the Story Layer Template.|
|scaleFactor|REAL|The scale to be assinged to any Layers created from this template.|
|layerLevelType|STRING|The Layer Level Type to be assigned to any Layers created from this template.|
|elevationOffset|REAL|The offset of the elevation of any Layer created from this template from the elevation of its Story.|
|defaultWallHeight|REAL|The wall height to be assigned to any Layer created from this template.|
|index|INTEGER|The index of the new template in the list of templates.|

## Examples
```pascal
VAR

success:BOOLEAN;

BEGIN

success := CreateStoryLayerTemplate('Mod-Slab', 1, 'LT_Slab', 0, 6);
```

```pascal
resultOK := CreateStoryLayerTemplate('Example', 1.0, 'Design Layer-1', 2.0, 0.5, 1);
```
```python
import vs

# Creates a Story Layer Template in the current file.
name = 'Example'
scaleFactor = 1.0
layerLevelType = 'Design Layer-1'
elevationOffset = 0.0
defaultWallHeight = 2.0

ok, index = vs.CreateStoryLayerTemplate(name, scaleFactor, layerLevelType, elevationOffset, defaultWallHeight)
vs.Message('CreateStoryLayerTemplate returned: ' + str((ok, index)))
```

## See Also
VS Functions:
[GetNumStoryLayerTemplates](GetNumStoryLayerTemplates.md) 
| [GetStoryLayerTemplateName](GetStoryLayerTemplateName.md) 
| [DeleteStoryLayerTemplate](DeleteStoryLayerTemplate.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
