# IFC_WriteProjectData

## Description
Writes specified field data to the Export IFC Project dialog.

```pascal
FUNCTION IFC_WriteProjectData(
				iPane     : INTEGER;
				iParam    : INTEGER;
				iBuilding : INTEGER;
				data      : STRING): BOOLEAN;
```

```python
def vs.IFC_WriteProjectData(iPane, iParam, iBuilding, data):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|iPane|INTEGER|   |
|iParam|INTEGER|   |
|iBuilding|INTEGER|   |
|data|STRING|   |

## Examples
```pascal
resultOK := IFC_WriteProjectData(1, 2, 3, 'Example');
```
```python
import vs

# Writes specified field data to the Export IFC Project dialog.
iPane = 1
iParam = 2
iBuilding = 3
data = 'Example'

ok = vs.IFC_WriteProjectData(iPane, iParam, iBuilding, data)
if ok:
    vs.Message('IFC_WriteProjectData succeeded')
else:
    vs.Message('IFC_WriteProjectData failed')
```

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
