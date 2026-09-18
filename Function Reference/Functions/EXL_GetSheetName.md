# EXL_GetSheetName

## Description
Get name of Excel sheets.

```pascal
FUNCTION EXL_GetSheetName(
				sheetIndex       : INTEGER;
				VAR outSheetName : STRING): BOOLEAN;
```

```python
def vs.EXL_GetSheetName(sheetIndex):
    return (BOOLEAN, outSheetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|outSheetName|STRING|   |

## Examples
```pascal
resultOK := EXL_GetSheetName(1, 'Example');
```
```python
import vs

# Get name of Excel sheets.
sheetIndex = 1

ok, outSheetName = vs.EXL_GetSheetName(sheetIndex)
vs.Message('EXL_GetSheetName returned: ' + str((ok, outSheetName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
