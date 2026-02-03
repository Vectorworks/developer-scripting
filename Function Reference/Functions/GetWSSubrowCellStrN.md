# GetWSSubrowCellStrN

## Description
Returns the displayed string in a database subrow cell.

```pascal
PROCEDURE GetWSSubrowCellStrN(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				subrow         : INTEGER;
				VAR cellString : DYNARRAY[] of CHAR);
```

```python
def vs.GetWSSubrowCellStrN(worksheet, row, column, subrow):
    return cellString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
|subrow|INTEGER|Index of subrow cell to be queried.|
|cellString|DYNARRAY[] of CHAR|Display string of subrow cell.|

## Remarks
Gets the specified worksheet subrow cell's displayed string.<BR>
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string, any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk.

## Examples
```pascal
PROCEDURE WStest;
   VAR
       autoRecalcState : BOOLEAN;
       worksheet : HANDLE;
       inString, outString : DYNARRAY [] OF CHAR;
BEGIN
   inString := '';
   outString := '';

   worksheet := CreateWS('MyWS', 5, 5);

   RectangleN(0, 0, 1, 0, 1, 1);

   {Save the current AutoRecalc state}
   autoRecalcState := GetWSAutoRecalcState(worksheet);

   {Turn off worksheet Auto Recalculation}
   SetWSAutoRecalcState(worksheet, false);

   { creates a database sub-row for the type 'RECT' }
   inString := '=DATABASE((T=RECT))';
   SetWSCellFormulaN(worksheet, 3, 0, 3, 0, inString);

   { inserts a formula into a database row cell }
   inString := '=T';
   SetWSCellFormulaN(worksheet, 3, 1, 3, 1, inString);

   {Restore AutoRecalc state}
   SetWSAutoRecalcState(worksheet, autoRecalcState);

   {Now recalculate the worksheet}
   RecalculateWS(worksheet);

   { gets subrow display string }
   GetWSSubrowCellStringN(worksheet, 3, 1, 1, outString);

   AlrtDialog(outString); { the subrow cell display string }
END;
RUN(WStest);
```

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
