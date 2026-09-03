# IFC_AddObjectMapping

## Description
Adds new object mapping to the specified category.

```pascal
FUNCTION IFC_AddObjectMapping(
				objectName : STRING;
				condition  : STRING;
				category   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_AddObjectMapping(objectName, condition, category):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|condition|STRING|   |
|category|INTEGER|   |

## Examples
```pascal
resultOK := IFC_AddObjectMapping('Example', 'Example', 1);
```
```python
import vs

# Adds new object mapping to the specified category.
objectName = 'Example'
condition = 'Example'
category = 1

ok = vs.IFC_AddObjectMapping(objectName, condition, category)
if ok:
    vs.Message('IFC_AddObjectMapping succeeded')
else:
    vs.Message('IFC_AddObjectMapping failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
