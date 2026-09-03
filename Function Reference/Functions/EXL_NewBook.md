# EXL_NewBook

## Description
Create a new Excel file.

```pascal
FUNCTION EXL_NewBook(filePath : STRING): BOOLEAN;
```

```python
def vs.EXL_NewBook(filePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|   |

## Examples
```pascal
resultOK := EXL_NewBook('file.txt');
```
```python
import vs

# Create a new Excel file.
filePath = 'C:/Temp'

ok = vs.EXL_NewBook(filePath)
if ok:
    vs.Message('EXL_NewBook succeeded')
else:
    vs.Message('EXL_NewBook failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
