# SetWSCellFormulaN

## Description
Inserts a formula into a cell of the referenced worksheet.

SetWSCellFormulaN allows a formula to be inserted into a rectangular range of cells. To insert a formula into a single cell, specify identical values for the top/bottom and left/right range boundaries.

SetWSCellFormulaN triggers a worksheet recalculation if the AutoRecalc flag is set.

It is best to turn off that flag before using SetWSCellFormulaN repeatedly or in a loop and restore the flag after all operations are done (see [ GetWSAutoRecalcState](GetWSAutoRecalcState.md) and [ SetWSAutoRecalcState](SetWSAutoRecalcState.md)).

At the end, the worksheet should be recalculated by calling [ RecalculateWS](RecalculateWS.md).

```pascal
PROCEDURE SetWSCellFormulaN(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				formula     : DYNARRAY[] of CHAR);
```

```python
def vs.SetWSCellFormulaN(worksheet, topRow, leftColumn, bottomRow, rightColumn, formula):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|topRow|INTEGER|Top row of cell insertion range.|
|leftColumn|INTEGER|Leftmost column of cell insertion range.|
|bottomRow|INTEGER|Bottom row of cell insertion range.|
|rightColumn|INTEGER|Rightmost column of cell insertion range.|
|formula|DYNARRAY[] of CHAR|Formula to be inserted into cell range.|

## Remarks
Sets specified formula string in specified worksheet cell(s).

If the 0 column is specified, a database row is created and the formula set as the database row criteria.

## Examples
```pascal
PROCEDURE WStest;
   VAR
       autoRecalcState : BOOLEAN;
       worksheet : HANDLE;
       inString : DYNARRAY [] OF CHAR;

BEGIN
   inString := '';

   worksheet := CreateWS('MyWS', 5, 5);

   RectangleN(0, 0, 1, 0, 1, 1);

   {Save the current AutoRecalc state}
   autoRecalcState := GetWSAutoRecalcState(worksheet);

   {Turn off worksheet Auto Recalculation}
   SetWSAutoRecalcState(worksheet, false);

   { inserts a formula into a single cell }
   inString := '=3*2';
   SetWSCellFormulaN(worksheet, 1, 2, 1, 2, inString);

   { inserts a formula into a range of cells }
   inString := '&lt;empty&gt;';
   SetWSCellFormulaN(worksheet, 1, 3, 2, 4, inString);

   { creates a database subrow for the type 'RECT' }
   inString := '=DATABASE((T=RECT))';
   SetWSCellFormulaN(worksheet, 3, 0, 3, 0, inString);

   { inserts a formula into a database row cell }
   inString := '=T';
   SetWSCellFormulaN(worksheet, 3, 1, 3, 1, inString);

   {Restore AutoRecalc state}
   SetWSAutoRecalcState(worksheet, autoRecalcState);

   {Now recalculate the worksheet}
   RecalculateWS(worksheet);
END;
RUN(WStest);
```

## See Also
VS Functions:
* [GetWSAutoRecalcState](GetWSAutoRecalcState.md) 
* [SetWSAutoRecalcState](SetWSAutoRecalcState.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Worksheets](../Categories/Worksheets.md)
