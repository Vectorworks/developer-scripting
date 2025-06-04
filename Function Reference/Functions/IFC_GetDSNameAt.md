# IFC_GetDSNameAt

## Description
Gets Data Sheets name for object at specified index.

```pascal
FUNCTION IFC_GetDSNameAt(
				objectName           : STRING;
				iDataSheet           : INTEGER;
				VAR outDataSheetName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetDSNameAt(objectName, iDataSheet):
    return (BOOLEAN, outDataSheetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|iDataSheet|INTEGER|   |
|outDataSheetName|STRING|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
