# EXL_GetCellAlignment

## Description
Get cell horizontal and vertical alignment, text angle, is text wrapped and is inconsistency found.

```pascal
FUNCTION EXL_GetCellAlignment(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				VAR outAlignmentH         : INTEGER;
				VAR outAlignmentV         : INTEGER;
				VAR outTextAngle          : INTEGER;
				VAR outWrapTextFlag       : BOOLEAN;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_GetCellAlignment(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outAlignmentH, outAlignmentV, outTextAngle, outWrapTextFlag, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outAlignmentH|INTEGER|   |
|outAlignmentV|INTEGER|   |
|outTextAngle|INTEGER|   |
|outWrapTextFlag|BOOLEAN|   |
|outInconsistencyFound|BOOLEAN|   |

## Examples
```pascal
resultOK := EXL_GetCellAlignment(1, 2, 3, 10, 5, 1, TRUE, FALSE);
```
```python
import vs

# Get cell horizontal and vertical alignment, text angle, is text wrapped and
# is inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outAlignmentH, outAlignmentV, outTextAngle, outWrapTextFlag, outInconsistencyFound = vs.EXL_GetCellAlignment(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellAlignment returned: ' + str((ok, outAlignmentH, outAlignmentV, outTextAngle, outWrapTextFlag, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
