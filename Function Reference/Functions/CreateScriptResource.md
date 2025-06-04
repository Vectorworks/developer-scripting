# CreateScriptResource

## Description
Create a document script resource.

```pascal
FUNCTION CreateScriptResource(
				scriptName  : STRING;
				paletteName : STRING;
				paletteOpen : BOOLEAN;
				script      : DYNARRAY[] of CHAR;
				python      : BOOLEAN): BOOLEAN;
```

```python
def vs.CreateScriptResource(scriptName, paletteName, paletteOpen, script, python):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|scriptName|STRING|A unique name for the new document script.|
|paletteName|STRING|A name of the script palette that will contain the new script. If the script palette doesn't exist, it will be created.|
|paletteOpen|BOOLEAN|Pass in TRUE if the script palette should be opened when created, and FALSE if it should be closed. If the palette exist, this parameter has no effect.|
|script|DYNARRAY[] of CHAR|The script text.|
|python|BOOLEAN|Pass TRUE if the script text contains python script. Otherwise it will be considered VectorScript.|

## See Also
VS Functions:
[GetScriptResource](GetScriptResource.md) 
| [SetScriptResource](SetScriptResource.md) 
| [OpenScriptResPal](OpenScriptResPal.md)

## Version
Availability: from Vectorworks 2014

## Category
* [General Edit](../Categories/General%20Edit.md)
