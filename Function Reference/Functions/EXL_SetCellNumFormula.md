# EXL_SetCellNumFormula

## Description
Write cell value as a numeric formula.

```pascal
FUNCTION EXL_SetCellNumFormula(
				sheetIndex    : INTEGER;
				cellRow       : INTEGER;
				cellColumn    : INTEGER;
				formulaString : STRING;
				formulaValue  : REAL): BOOLEAN;
```

```python
def vs.EXL_SetCellNumFormula(sheetIndex, cellRow, cellColumn, formulaString, formulaValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|formulaString|STRING|   |
|formulaValue|REAL|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
