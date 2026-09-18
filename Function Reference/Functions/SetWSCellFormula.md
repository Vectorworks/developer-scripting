# SetWSCellFormula

## Description
Inserts a formula into a cell of the referenced worksheet.

SetWSCellFormula allows a formula to be inserted into a rectangular range of cells. To insert a formula into a single cell, specify identical values for the top/bottom and left/right range boundaries.

```pascal
PROCEDURE SetWSCellFormula(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				formula     : STRING);
```

```python
def vs.SetWSCellFormula(worksheet, topRow, leftColumn, bottomRow, rightColumn, formula):
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
|formula|STRING|Formula to be inserted into cell range.|

## Remarks
Sets specified formula string in specified worksheet cell(s).
If the 0 column is specified, a database row is created and the formula set as the database row criteria.

## Examples
#### VectorScript ####
```pascal
{ inserts a formula into a single cell }
SetWSCellFormula(h,4,2,4,2,'=3*2');

{ inserts a formula into a range of cells }
SetWSCellFormula(h,1,1,2,10,'<empty>');

{ creates a database sub-row for the record 'Part Info' }
SetWSCellFormula(h,2,0,2,0,'=DATABASE(R IN [''PART INFO''])');
```
#### Python ####
```python

```

```pascal
{Cells}
SetWSCellTextFormat(tempHandle,1,1,1,1,DefaultWSFontID,14,1);
SetWSCellNumberFormat(tempHandle,1,1,1,1,0,0,'','');
SetWSCellBorder(tempHandle,1,1,1,1,TRUE,TRUE,FALSE,FALSE,FALSE);
SetWSCellFormula(tempHandle,1,1,1,1,kRLwkshtName);

SetWSCellTextFormat(MyWSHandle, 3, 1, 3, 5, DefaultWSFontID, 12, 1); {Bold 12pt for row 3}
SetWSCellFormula   (MyWSHandle, 3, 1, 3, 1, kTotal);
SetWSCellAlignment (MyWSHandle, 3, 1, 3, 1, 3); {Right Align}

	SetTopVisibleWS( WSh );
	{SelectSS(hWS);{activate and Open to Show single change}
	GetWSCellTextFormat( WSh, row, col, fontIdx, fontSize, fontStyle );
	ReplaceStr(str,gFindString,gReplString,gCase);
	SetWSCellFormula( WSh, row, col, row, col, gResultText );
	SetWSCellTextFormat(WSh,row,col,row,col,fontIdx,fontSize,fontStyle);
	ProcessFoundCell := TRUE;
END;
```
```python
vs.SetWSCellFormula(worksheet, topRow, leftColumn, bottomRow, rightColumn, formula)
```
See also in tutorials: [21. Hello Worksheet — Create and Populate](ai%20examples/21_WorksheetBasic.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
