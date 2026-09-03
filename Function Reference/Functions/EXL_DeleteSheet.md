# EXL_DeleteSheet

## Description
Delete the sheet with the specified name.

```pascal
FUNCTION EXL_DeleteSheet(sheetName : STRING): BOOLEAN;
```

```python
def vs.EXL_DeleteSheet(sheetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetName|STRING|   |

## Examples
```pascal
resultOK := EXL_DeleteSheet('Example');
```
```python
import vs

# Delete the sheet with the specified name.
sheetName = 'Example'

ok = vs.EXL_DeleteSheet(sheetName)
if ok:
    vs.Message('EXL_DeleteSheet succeeded')
else:
    vs.Message('EXL_DeleteSheet failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
