# GetWSCellFormulaN

## Description
Returns the formula from a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellFormulaN(
				worksheet   : HANDLE;
				row         : INTEGER;
				column      : INTEGER;
				VAR formula : DYNARRAY[] of CHAR);
```

```python
def vs.GetWSCellFormulaN(worksheet, row, column):
    return formula
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|formula|DYNARRAY[] of CHAR|Formula contained in worksheet cell.|

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

   { gets formula from cell }
   GetWSCellFormulaN(worksheet, 1, 2, outString);

   AlrtDialog(outString); { the cell formula }
END;
RUN(WStest);
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
