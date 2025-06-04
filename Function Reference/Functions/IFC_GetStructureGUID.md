# IFC_GetStructureGUID

## Description
Gets specified GUID.

```pascal
FUNCTION IFC_GetStructureGUID(
				guidType    : INTEGER;
				iBuilding   : INTEGER;
				iStorey     : INTEGER;
				VAR outGuid : STRING): BOOLEAN;
```

```python
def vs.IFC_GetStructureGUID(guidType, iBuilding, iStorey):
    return (BOOLEAN, outGuid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|guidType|INTEGER|   |
|iBuilding|INTEGER|   |
|iStorey|INTEGER|   |
|outGuid|STRING|   |

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
