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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
