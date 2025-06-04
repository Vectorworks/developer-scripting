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

## Version
Availability: from VectorWorks12.5

## Category
* [Worksheets](../Categories/Worksheets.md)
