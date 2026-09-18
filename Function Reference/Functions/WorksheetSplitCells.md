# WorksheetSplitCells

## Description
Splits the specified cells back into individual cells.

```pascal
FUNCTION WorksheetSplitCells(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER): BOOLEAN;
```

```python
def vs.WorksheetSplitCells(worksheet, topRow, leftColumn, bottomRow, rightColumn):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Worksheet on which function is to operate.|
|topRow|INTEGER|Top row of range to split.|
|leftColumn|INTEGER|Left column of range to split.|
|bottomRow|INTEGER|Bottom row of range to split.|
|rightColumn|INTEGER|Right column of range to split.|

## Examples
```pascal
resultOK := WorksheetSplitCells(worksheet, 1, 2, 3, 10);
```
```python
import vs

# Splits the specified cells back into individual cells.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5

ok = vs.WorksheetSplitCells(worksheet, topRow, leftColumn, bottomRow, rightColumn)
if ok:
    vs.Message('WorksheetSplitCells succeeded')
else:
    vs.Message('WorksheetSplitCells failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Worksheets](../Categories/Worksheets.md)
