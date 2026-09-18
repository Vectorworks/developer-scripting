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

## Examples
```pascal
resultOK := EXL_GetCellFill(1, 2, 3, 10, 5, 1, 2, TRUE);
```
```python
import vs

# Get cell fill style, background color, foreground color, fill pattern and
# is inconsistency found.
sheetIndex = 1
cellRow = 10
cellColumn = 5

ok, outStyle, outBgColor, outFgColor, outFillpattern, outInconsistencyFound = vs.EXL_GetCellFill(sheetIndex, cellRow, cellColumn)
vs.Message('EXL_GetCellFill returned: ' + str((ok, outStyle, outBgColor, outFgColor, outFillpattern, outInconsistencyFound)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Excel](../Categories/Excel.md)
