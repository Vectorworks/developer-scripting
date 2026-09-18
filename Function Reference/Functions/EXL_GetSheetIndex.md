# EXL_GetSheetIndex

## Description
Gets index of the Excel sheet.

```pascal
FUNCTION EXL_GetSheetIndex(
				sheetName         : STRING;
				VAR outSheetIndex : INTEGER): BOOLEAN;
```

```python
def vs.EXL_GetSheetIndex(sheetName):
    return (BOOLEAN, outSheetIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetName|STRING|   |
|outSheetIndex|INTEGER|   |

## Examples
```pascal
resultOK := EXL_GetSheetIndex('Example', 1);
```
```python
import vs

# Gets index of the Excel sheet.
sheetName = 'Example'

ok, outSheetIndex = vs.EXL_GetSheetIndex(sheetName)
vs.Message('EXL_GetSheetIndex returned: ' + str((ok, outSheetIndex)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
