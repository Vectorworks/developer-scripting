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

## Examples
```pascal
resultOK := IFC_GetStructureGUID(1, 2, 3, 'Example');
```
```python
import vs

# Gets specified GUID.
guidType = 0
iBuilding = 1
iStorey = 2

ok, outGuid = vs.IFC_GetStructureGUID(guidType, iBuilding, iStorey)
vs.Message('IFC_GetStructureGUID returned: ' + str((ok, outGuid)))
```

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
