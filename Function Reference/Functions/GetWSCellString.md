# GetWSCellString

## Description
Returns the displayed string value of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellString(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				VAR cellString : STRING);
```

```python
def vs.GetWSCellString(worksheet, row, column):
    return cellString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|cellString|STRING|The string value contained in the worksheet cell.|

## Remarks
Gets the specified worksheet cell's displayed string.
If the cell contains a string, the displayed string IS that string.
If the cell contains a number, the displayed string is that number PLUS any formatting applied to that number.
Use [[VS:IsWSCellNumber| IsWSCellString]] and/or [[VS:IsWSCellNumber| IsWSCellNumber]] to determine what type of value the cell actually contains. 
Use [[VS:GetWSCellValue| GetWSCellValue]] to retrieve actual numerical value without formatting from a cell that contains a number.

## See Also
[IsWSCellString | IsWSCellString](IsWSCellString%20| IsWSCellString.md), [IsWSCellStringN | IsWSCellStringN](IsWSCellStringN%20| IsWSCellStringN.md), [IsWSCellNumber | IsWSCellNumber](IsWSCellNumber%20| IsWSCellNumber.md), [GetWSCellValue | GetWSCellValue](GetWSCellValue%20| GetWSCellValue.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
