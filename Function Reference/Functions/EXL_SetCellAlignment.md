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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
