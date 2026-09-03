# IFC_ExportNoUI

## Description
Exports IFC file, without showing Export IFC Project dialog.

```pascal
FUNCTION IFC_ExportNoUI(strFullFilePath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.IFC_ExportNoUI(strFullFilePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strFullFilePath|DYNARRAY[] of CHAR|   |

## Examples
```pascal
resultOK := IFC_ExportNoUI(strFullFilePath);
```
```python
import vs

# Exports IFC file, without showing Export IFC Project dialog.
strFullFilePath = 'C:/Temp'

ok = vs.IFC_ExportNoUI(strFullFilePath)
if ok:
    vs.Message('IFC_ExportNoUI succeeded')
else:
    vs.Message('IFC_ExportNoUI failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
