# IFC_DeleteObjectMap

## Description
Deletes mapping for object.

```pascal
FUNCTION IFC_DeleteObjectMap(objectName : STRING): BOOLEAN;
```

```python
def vs.IFC_DeleteObjectMap(objectName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |

## Examples
```pascal
resultOK := IFC_DeleteObjectMap('Example');
```
```python
import vs

# Deletes mapping for object.
objectName = 'Example'

ok = vs.IFC_DeleteObjectMap(objectName)
if ok:
    vs.Message('IFC_DeleteObjectMap succeeded')
else:
    vs.Message('IFC_DeleteObjectMap failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
