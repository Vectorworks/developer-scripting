# EXL_IsCellValid

## Description
Check is cell in range of Excel sheets.

```pascal
FUNCTION EXL_IsCellValid(
				sheetIndex : INTEGER;
				cellRow    : INTEGER;
				cellColumn : INTEGER): BOOLEAN;
```

```python
def vs.EXL_IsCellValid(sheetIndex, cellRow, cellColumn):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |

## Examples
```pascal
resultOK := EXL_IsCellValid(1, 2, 3);
```
```python
import vs

# Check is cell in range of Excel sheets.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok = vs.EXL_IsCellValid(sheetIndex, cellRow, cellColumn)
if ok:
    vs.Message('EXL_IsCellValid succeeded')
else:
    vs.Message('EXL_IsCellValid failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
