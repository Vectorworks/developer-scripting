# IFC_ReadProjectData

## Description
Reads specified field data from the Export IFC Project dialog.

```pascal
FUNCTION IFC_ReadProjectData(
				iPane       : INTEGER;
				iParam      : INTEGER;
				iBuilding   : INTEGER;
				VAR outData : STRING): BOOLEAN;
```

```python
def vs.IFC_ReadProjectData(iPane, iParam, iBuilding):
    return (BOOLEAN, outData)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|iPane|INTEGER|   |
|iParam|INTEGER|   |
|iBuilding|INTEGER|   |
|outData|STRING|   |

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
