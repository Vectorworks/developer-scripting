# EXL_SetCellAlignment

## Description
Set cell horizontal and vertical alignment, text angle, is text wrapped and is inconsistency found.

```pascal
FUNCTION EXL_SetCellAlignment(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				AlignmentH                : INTEGER;
				AlignmentV                : INTEGER;
				TextAngle                 : INTEGER;
				WrapTextFlag              : BOOLEAN;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_SetCellAlignment(sheetIndex, cellRow, cellColumn, AlignmentH, AlignmentV, TextAngle, WrapTextFlag):
    return (BOOLEAN, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|AlignmentH|INTEGER|   |
|AlignmentV|INTEGER|   |
|TextAngle|INTEGER|   |
|WrapTextFlag|BOOLEAN|   |
|outInconsistencyFound|BOOLEAN|   |

## Examples
```pascal
resultOK := EXL_SetCellAlignment(1, 2, 3, 10, 5, 1, TRUE, FALSE);
```
```python
import vs

# Set cell horizontal and vertical alignment, text angle, is text wrapped and
# is inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5
AlignmentH = 1
AlignmentV = 2
TextAngle = 3
WrapTextFlag = True

ok, outInconsistencyFound = vs.EXL_SetCellAlignment(sheetIndex, cellRow, cellColumn, AlignmentH, AlignmentV, TextAngle, WrapTextFlag)
vs.Message('EXL_SetCellAlignment returned: ' + str((ok, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
