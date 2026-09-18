# IFC_DeleteDSField

## Description
Deletes field from Data Sheet.

```pascal
FUNCTION IFC_DeleteDSField(
				objectName    : STRING;
				dataSheetName : STRING;
				fieldLabel    : STRING): BOOLEAN;
```

```python
def vs.IFC_DeleteDSField(objectName, dataSheetName, fieldLabel):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|fieldLabel|STRING|   |

## Examples
```pascal
resultOK := IFC_DeleteDSField('Example', 'Example', 'MyRecord');
```
```python
import vs

# Deletes field from Data Sheet.
objectName = 'Example'
dataSheetName = 'Example'
fieldLabel = 'MyField'

ok = vs.IFC_DeleteDSField(objectName, dataSheetName, fieldLabel)
if ok:
    vs.Message('IFC_DeleteDSField succeeded')
else:
    vs.Message('IFC_DeleteDSField failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
