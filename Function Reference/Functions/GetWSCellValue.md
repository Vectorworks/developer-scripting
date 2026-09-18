# GetWSCellValue

## Description
Returns the displayed numeric value of a cell in the referenced worksheet.

```pascal
PROCEDURE GetWSCellValue(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR cellValue : REAL);
```

```python
def vs.GetWSCellValue(worksheet, row, column):
    return cellValue
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|cellValue|REAL|Numeric value contained in worksheet cell.|

## Examples
```pascal
BEGIN
	GetWSCellValue (wksHand, row, col+1, tempInt);	{pen color}
	ColorIndexToRGB (tempInt, r, g, b);
	SetClPenFore (userClassName, r, g, b);

{* Get the class properties *}
col := gNumClassStds;
GetWSCellValue (gClassWSHandle, 1+i, col+1, colorIndex);
gClassList [i].PenColor := colorIndexToDecimal (colorIndex);
GetWSCellValue (gClassWSHandle, 1+i, col+2, gClassList [i].LW);
GetWSCellValue (gClassWSHandle, 1+i, col+3, pseudoIndex);
convertStatus := GetDashFromPseudoInd(pseudoIndex, gClassList [i].LS);

BEGIN
	row := row + 1;
	GetWSCellString (wksH1, row, 2, curveTypeS [i]);
	curveType [i] := Str2Num (Copy (curveTypeS [i], 1, 1));
	GetWSCellValue (wksH1, row, 3, endAngle [i]);
	GetWSCellValue (wksH1, row, 4, endDisp [i]);
END;
```
```python
if classFound:
	tempInt = vs.GetWSCellValue( wksHand, row, col + 1 )
	# pen color
	r, g, b = vs.ColorIndexToRGB( tempInt )
	vs.SetClPenFore( userClassName, r, g, b )
	tempInt = vs.GetWSCellValue( wksHand, row, col + 2 )
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
