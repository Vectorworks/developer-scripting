# EXL_SaveAndCloseBook

## Description
Save and closes the Excel file.

```pascal
FUNCTION EXL_SaveAndCloseBook(filePath : STRING): BOOLEAN;
```

```python
def vs.EXL_SaveAndCloseBook(filePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|   |

## Examples
```pascal
resultOK := EXL_SaveAndCloseBook('file.txt');
```
```python
import vs

# Save and closes the Excel file.
filePath = 'C:/Temp'

ok = vs.EXL_SaveAndCloseBook(filePath)
if ok:
    vs.Message('EXL_SaveAndCloseBook succeeded')
else:
    vs.Message('EXL_SaveAndCloseBook failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
