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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
