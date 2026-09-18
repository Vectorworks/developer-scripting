# EXL_GetSheetCnt

## Description
Get counts of Excel sheets.

```pascal
FUNCTION EXL_GetSheetCnt(VAR outSheetCount : INTEGER): BOOLEAN;
```

```python
def vs.EXL_GetSheetCnt():
    return (BOOLEAN, outSheetCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outSheetCount|INTEGER|   |

## Examples
```pascal
resultOK := EXL_GetSheetCnt(1);
```
```python
import vs

# Get counts of Excel sheets.
ok, outSheetCount = vs.EXL_GetSheetCnt()
vs.Message('EXL_GetSheetCnt returned: ' + str((ok, outSheetCount)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
