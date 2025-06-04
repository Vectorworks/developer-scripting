# IFC_GetDSFieldsCount

## Description
Gets Data Sheet's fields count.

```pascal
FUNCTION IFC_GetDSFieldsCount(
				objectName         : STRING;
				dataSheetName      : STRING;
				VAR outFieldsCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetDSFieldsCount(objectName, dataSheetName):
    return (BOOLEAN, outFieldsCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|outFieldsCount|INTEGER|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
