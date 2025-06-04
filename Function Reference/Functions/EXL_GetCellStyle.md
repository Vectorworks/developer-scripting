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

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
