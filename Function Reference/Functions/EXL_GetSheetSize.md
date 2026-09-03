# EXL_GetSheetSize

## Description
Get size of Excel sheets.

```pascal
FUNCTION EXL_GetSheetSize(
				sheetIndex     : INTEGER;
				VAR outRows    : INTEGER;
				VAR outColumns : INTEGER): BOOLEAN;
```

```python
def vs.EXL_GetSheetSize(sheetIndex):
    return (BOOLEAN, outRows, outColumns)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|outRows|INTEGER|   |
|outColumns|INTEGER|   |

## Examples
```pascal
resultOK := EXL_GetSheetSize(1, 2, 3);
```
```python
import vs

# Get size of Excel sheets.
sheetIndex = 1

ok, outRows, outColumns = vs.EXL_GetSheetSize(sheetIndex)
vs.Message('EXL_GetSheetSize returned: ' + str((ok, outRows, outColumns)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
