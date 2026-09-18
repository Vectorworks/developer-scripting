# EXL_GetCellStyle

## Description
Get cell number style class, accuracy and is inconsistency found.

```pascal
FUNCTION EXL_GetCellStyle(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				VAR outNumStyleClass      : INTEGER;
				VAR outAccuracy           : INTEGER;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_GetCellStyle(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outNumStyleClass, outAccuracy, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outNumStyleClass|INTEGER|   |
|outAccuracy|INTEGER|   |
|outInconsistencyFound|BOOLEAN|   |

## Examples
```pascal
resultOK := EXL_GetCellStyle(1, 2, 3, 10, 5, TRUE);
```
```python
import vs

# Get cell number style class, accuracy and is inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outNumStyleClass, outAccuracy, outInconsistencyFound = vs.EXL_GetCellStyle(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellStyle returned: ' + str((ok, outNumStyleClass, outAccuracy, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
