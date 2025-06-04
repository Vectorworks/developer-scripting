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

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
