# GetWSCellStringN

## Description
Returns the displayed string value of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellStringN(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				VAR cellString : DYNARRAY[] of CHAR);
```

```python
def vs.GetWSCellStringN(worksheet, row, column):
    return cellString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|cellString|DYNARRAY[] of CHAR|The string value contained in the worksheet cell.|

## Remarks
Gets the specified worksheet cell's displayed string.<BR>
If the cell contains a string, the displayed string IS that string.<BR>
If the cell contains a number, the displayed string is that number PLUS any formatting applied to that number.<BR>
Use IsWSCellString and/or MP_IsWSCellNumber to determine what type of value the cell actually contains. <BR>
Use GetWSCellValue to retrieve actual numerical value without formatting from a cell that contains a number.

## Examples
```pascal
PROCEDURE WStest;
    VAR
       worksheet : HANDLE;
       inString, outString : DYNARRAY [] OF CHAR;
BEGIN
   worksheet := CreateWS('MyWS', 5, 5);
   inString := '';
   outString := '';

   { inserts a formula into a single cell }
   inString := '=3*2';
   SetWSCellFormulaN(worksheet, 1, 2, 1, 2, inString);

   { gets string from cell }
   GetWSCellStringN(worksheet, 1, 2, outString);

   AlrtDialog(outString); { the cell formula }
END;
RUN(WStest);
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
