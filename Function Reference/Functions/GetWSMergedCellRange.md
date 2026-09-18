# GetWSMergedCellRange

## Description
Gets the range of cells covered by the specified cell. Returns true if the specified cell is a merged cell.

```pascal
FUNCTION GetWSMergedCellRange(
				worksheet       : HANDLE;
				row             : INTEGER;
				column          : INTEGER;
				VAR topRow      : INTEGER;
				VAR leftColumn  : INTEGER;
				VAR bottomRow   : INTEGER;
				VAR rightColumn : INTEGER): BOOLEAN;
```

```python
def vs.GetWSMergedCellRange(worksheet, row, column):
    return (BOOLEAN, topRow, leftColumn, bottomRow, rightColumn)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Worksheet on which function is to operate.|
|row|INTEGER|Row index of merged cell from which to get the covered range.|
|column|INTEGER|Column index of merged cell from which to get the covered range.|
|topRow|INTEGER|Top row index of merged cell range.|
|leftColumn|INTEGER|Left column index of merged cell range.|
|bottomRow|INTEGER|Bottom row index of merged cell range.|
|rightColumn|INTEGER|Right column index of merged cell range.|

## Examples
```pascal
resultOK := GetWSMergedCellRange(worksheet, 1, 2, 3, 10, 5, 1);
```
```python
import vs

# Gets the range of cells covered by the specified cell.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

ok, topRow, leftColumn, bottomRow, rightColumn = vs.GetWSMergedCellRange(worksheet, row, column)
vs.Message('GetWSMergedCellRange returned: ' + str((ok, topRow, leftColumn, bottomRow, rightColumn)))
```

## Version
Availability: from VectorWorks12.5

## Category
* [Worksheets](../Categories/Worksheets.md)
