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

## Examples
```pascal
resultOK := IFC_ReadProjectData(1, 2, 3, 'Example');
```
```python
import vs

# Reads specified field data from the Export IFC Project dialog.
iPane = 1
iParam = 2
iBuilding = 3

ok, outData = vs.IFC_ReadProjectData(iPane, iParam, iBuilding)
vs.Message('IFC_ReadProjectData returned: ' + str((ok, outData)))
```

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
