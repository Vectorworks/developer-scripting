# IsValidWSCell

## Description
Returns if a specified cell is within the valid range of the referenced worksheet.

```pascal
FUNCTION IsValidWSCell(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.IsValidWSCell(worksheet, row, column):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of target cell.|
|column|INTEGER|Column of target cell.|

## Remarks
Determines if specified cell is valid for the specified worksheet.
NOTE: A determination that a cell is valid only means that the specified cell falls within a range of 0 to the current number of worksheet rows and 0 to the current number of worksheet columns. A valid cell does not imply that every worksheet SDK function will accept that cell. The user should always  note any specific cell and cell range restrictions of a call they may use.

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
