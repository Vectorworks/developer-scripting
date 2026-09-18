# IFC_SetStructureGUID

## Description
Sets specified GUID.

```pascal
FUNCTION IFC_SetStructureGUID(
				guidType  : INTEGER;
				iBuilding : INTEGER;
				iStorey   : INTEGER;
				Guid      : STRING): BOOLEAN;
```

```python
def vs.IFC_SetStructureGUID(guidType, iBuilding, iStorey, Guid):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|guidType|INTEGER|   |
|iBuilding|INTEGER|   |
|iStorey|INTEGER|   |
|Guid|STRING|   |

## Examples
```pascal
resultOK := IFC_SetStructureGUID(1, 2, 3, 'Example');
```
```python
import vs

# Sets specified GUID.
guidType = 0
iBuilding = 1
iStorey = 2
Guid = 'Example'

ok = vs.IFC_SetStructureGUID(guidType, iBuilding, iStorey, Guid)
if ok:
    vs.Message('IFC_SetStructureGUID succeeded')
else:
    vs.Message('IFC_SetStructureGUID failed')
```

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
