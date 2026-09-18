# IFC_CreateDS

## Description
Creates Data Sheet for object.

```pascal
FUNCTION IFC_CreateDS(
				objectName    : STRING;
				dataSheetName : STRING): BOOLEAN;
```

```python
def vs.IFC_CreateDS(objectName, dataSheetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |

## Examples
```pascal
resultOK := IFC_CreateDS('Example', 'Example');
```
```python
import vs

# Creates Data Sheet for object.
objectName = 'Example'
dataSheetName = 'Example'

ok = vs.IFC_CreateDS(objectName, dataSheetName)
if ok:
    vs.Message('IFC_CreateDS succeeded')
else:
    vs.Message('IFC_CreateDS failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
