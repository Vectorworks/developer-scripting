# EXL_AddSheet

## Description
Add a sheet. If a sheet with this name exists, it will be overwritten.

```pascal
FUNCTION EXL_AddSheet(sheetName : STRING): BOOLEAN;
```

```python
def vs.EXL_AddSheet(sheetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetName|STRING|   |

## Examples
```pascal
resultOK := EXL_AddSheet('Example');
```
```python
import vs

# Add a sheet.
sheetName = 'Example'

ok = vs.EXL_AddSheet(sheetName)
if ok:
    vs.Message('EXL_AddSheet succeeded')
else:
    vs.Message('EXL_AddSheet failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
