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
Use [ IsWSCellString](IsWSCellNumber.md) and/or [ IsWSCellNumber](IsWSCellNumber.md) to determine what type of value the cell actually contains. 
Use [ GetWSCellValue](GetWSCellValue.md) to retrieve actual numerical value without formatting from a cell that contains a number.

## Examples
```pascal
end else BEGIN
	{check each string cell for the string}
	FOR j := 1 to cols DO BEGIN
		if ( IsWSCellString(hWS,i,j) ) then BEGIN
			GetWSCellString( hWS, i, j, cellStr );
			IF ( FindString( cellStr ,gFindString,1,gCase) > 0 )
				then IF ( ProcessFoundCell( hWS, i, j, cellStr ) ) then BEGIN
					SearchWorksheet := TRUE;
					GOTO 98;

BEGIN
	GetWSCellString (wksHand, i+1, 1, tempStr);
	IF tempStr = defaultClassName THEN
	BEGIN
		GetWSCellString (wksHand, i+1, userIndex, userClassName);
		i := numClasses;

BEGIN
	wksHand := Getobject(GetLocStr (12017, 4));
	IF (wksHand<> NIL) THEN BEGIN
		FOR i := 1 TO kNumSheetDefs DO BEGIN
			getWSCellString (wksHand,kWSShtTypeRow,i+1,tempStr);
			tempInt := ord (tempStr);
			CASE tempInt OF
				49      : sheetType := 2;
				65, 76  : sheetType := 4;
```
```python
while (i <= numClasses ):
	tempStr = vs.GetWSCellString( wksHand, i + 1, userIndex )
	classFound = ( tempStr == userClassName )
	if classFound:
		row = i + 1
		i = numClasses
```

## See Also
[IsWSCellString](IsWSCellString.md), IsWSCellStringN, [ IsWSCellNumber](IsWSCellNumber.md), [GetWSCellValue](GetWSCellValue.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
