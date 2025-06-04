# SetScriptResource

## Description
Set the script text of the specified script resource.

```pascal
FUNCTION SetScriptResource(
				scriptName : STRING;
				script     : DYNARRAY[] of CHAR;
				python     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetScriptResource(scriptName, script, python):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|scriptName|STRING|The script name identifying the resource.|
|script|DYNARRAY[] of CHAR|The script text.|
|python|BOOLEAN|Pass TRUE if the script text contains python script. Otherwise it will be considered VectorScript.|

## See Also
VS Functions:
[CreateScriptResource](CreateScriptResource.md) 
| [GetScriptResource](GetScriptResource.md) 
| [OpenScriptResPal](OpenScriptResPal.md)

## Version
Availability: from Vectorworks 2014

## Category
* [General Edit](../Categories/General%20Edit.md)
