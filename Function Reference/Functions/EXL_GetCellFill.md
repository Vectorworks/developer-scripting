# EXL_GetCellFill

## Description
Get cell fill style, background color, foreground color, fill pattern and is inconsistency found.

```pascal
FUNCTION EXL_GetCellFill(
				sheetIndex                : INTEGER;
				cellRow                   : INTEGER;
				cellColumn                : INTEGER;
				VAR outStyle              : INTEGER;
				VAR outBgColor            : INTEGER;
				VAR outFgColor            : INTEGER;
				VAR outFillpattern        : INTEGER;
				VAR outInconsistencyFound : BOOLEAN): BOOLEAN;
```

```python
def vs.EXL_GetCellFill(sheetIndex, cellRow, cellColumn):
    return (BOOLEAN, outStyle, outBgColor, outFgColor, outFillpattern, outInconsistencyFound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|   |
|cellRow|INTEGER|   |
|cellColumn|INTEGER|   |
|outStyle|INTEGER|   |
|outBgColor|INTEGER|   |
|outFgColor|INTEGER|   |
|outFillpattern|INTEGER|   |
|outInconsistencyFound|BOOLEAN|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
