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

## Examples
```pascal
resultOK := EXL_SetCellNumFormula(1, 2, 3, 'Example', 1.0);
```
```python
import vs

# Write cell value as a numeric formula.
sheetIndex = 1
cellRow = 10
cellColumn = 5
formulaString = 'Example'
formulaValue = 1.0

ok = vs.EXL_SetCellNumFormula(sheetIndex, cellRow, cellColumn, formulaString, formulaValue)
if ok:
    vs.Message('EXL_SetCellNumFormula succeeded')
else:
    vs.Message('EXL_SetCellNumFormula failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
