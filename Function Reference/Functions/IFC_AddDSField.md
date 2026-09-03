# IFC_AddDSField

## Description
Adds field to a Data Sheet.

```pascal
FUNCTION IFC_AddDSField(
				objectName    : STRING;
				dataSheetName : STRING;
				mainEntry     : STRING;
				childEntry    : STRING;
				fieldName     : STRING;
				fieldLabel    : STRING): BOOLEAN;
```

```python
def vs.IFC_AddDSField(objectName, dataSheetName, mainEntry, childEntry, fieldName, fieldLabel):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|mainEntry|STRING|   |
|childEntry|STRING|   |
|fieldName|STRING|   |
|fieldLabel|STRING|   |

## Examples
```pascal
resultOK := IFC_AddDSField('Example', 'Example', 'Example', 'Example', 'MyRecord', 'MyRecord');
```
```python
import vs

# Adds field to a Data Sheet.
objectName = 'Example'
dataSheetName = 'Example'
mainEntry = 'Example'
childEntry = 'Example'
fieldName = 'MyField'
fieldLabel = 'MyField'

ok = vs.IFC_AddDSField(objectName, dataSheetName, mainEntry, childEntry, fieldName, fieldLabel)
if ok:
    vs.Message('IFC_AddDSField succeeded')
else:
    vs.Message('IFC_AddDSField failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
