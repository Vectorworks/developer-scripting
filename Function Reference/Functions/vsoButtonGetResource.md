# vsoButtonGetResource

## Description
Show a resource popup from the current shape pane button (while handing action 35: {ParametricUIButtonHitMessage::kAction}). Parameter name is a string that will receive the resource name.

```pascal
FUNCTION vsoButtonGetResource(
				paramName  : STRING;
				objectType : INTEGER;
				folderSpec : INTEGER;
				folderName : STRING): BOOLEAN;
```

```python
def vs.vsoButtonGetResource(paramName, objectType, folderSpec, folderName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paramName|STRING|   |
|objectType|INTEGER|   |
|folderSpec|INTEGER|   |
|folderName|STRING|   |

## Version
Availability: from Vectorworks 2018

## Category
* [Object Events](../Categories/Object%20Events.md)
