# IFC_DeleteDS

## Description
Deletes Data Sheet from object.

```pascal
FUNCTION IFC_DeleteDS(
				objectName    : STRING;
				dataSheetName : STRING): BOOLEAN;
```

```python
def vs.IFC_DeleteDS(objectName, dataSheetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |

## Examples
```pascal
resultOK := IFC_DeleteDS('Example', 'Example');
```
```python
import vs

# Deletes Data Sheet from object.
objectName = 'Example'
dataSheetName = 'Example'

ok = vs.IFC_DeleteDS(objectName, dataSheetName)
if ok:
    vs.Message('IFC_DeleteDS succeeded')
else:
    vs.Message('IFC_DeleteDS failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
