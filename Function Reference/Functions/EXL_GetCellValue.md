# EXL_GetCellValue

## Description
Get cell formula, string, leader string, trailer string and value.

```pascal
FUNCTION EXL_GetCellValue(
				sheetIndex        : INTEGER;
				cellRow           : INTEGER;
				cellColumn        : INTEGER;
				VAR outFormula    : STRING;
				VAR outString     : STRING;
				VAR outLeaderStr  : STRING;
				VAR outTrailerStr : STRING;
				VAR outValue      : REAL): BOOLEAN;
```

```python
def vs.EXL_GetCellValue(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outFormula, outString, outLeaderStr, outTrailerStr, outValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outFormula|STRING|   |
|outString|STRING|   |
|outLeaderStr|STRING|   |
|outTrailerStr|STRING|   |
|outValue|REAL|   |

## Examples
```pascal
resultOK := EXL_GetCellValue(1, 2, 3, 'Example', 'Example', 'Example', 'Example', 1.0);
```
```python
import vs

# Get cell formula, string, leader string, trailer string and value.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outFormula, outString, outLeaderStr, outTrailerStr, outValue = vs.EXL_GetCellValue(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellValue returned: ' + str((ok, outFormula, outString, outLeaderStr, outTrailerStr, outValue)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
