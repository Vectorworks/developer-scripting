# WorksheetMergeCells

## Description
Merges the specified cells into a single cell.

```pascal
FUNCTION WorksheetMergeCells(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER): BOOLEAN;
```

```python
def vs.WorksheetMergeCells(worksheet, topRow, leftColumn, bottomRow, rightColumn):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Worksheet on which function is to operate.|
|topRow|INTEGER|Top row of range to merge.|
|leftColumn|INTEGER|Left column of range to merge.|
|bottomRow|INTEGER|Bottom row of range to merge.|
|rightColumn|INTEGER|Right column of range to merge.|

## Version
Availability: from VectorWorks12.5

## Category
* [Worksheets](../Categories/Worksheets.md)
