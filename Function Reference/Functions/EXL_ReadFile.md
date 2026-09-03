# EXL_ReadFile

## Description
Read Excel file.

```pascal
FUNCTION EXL_ReadFile(FilePath : STRING): BOOLEAN;
```

```python
def vs.EXL_ReadFile(FilePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|FilePath|STRING|   |

## Examples
```pascal
resultOK := EXL_ReadFile('file.txt');
```
```python
import vs

# Read Excel file.
FilePath = 'C:/Temp'

ok = vs.EXL_ReadFile(FilePath)
if ok:
    vs.Message('EXL_ReadFile succeeded')
else:
    vs.Message('EXL_ReadFile failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
