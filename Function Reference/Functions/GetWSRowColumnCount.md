# GetWSRowColumnCount

## Description
Returns the number of rows and columns in the referenced worksheet.

```pascal
PROCEDURE GetWSRowColumnCount(
				worksheet      : HANDLE;
				VAR numRows    : INTEGER;
				VAR numColumns : INTEGER);
```

```python
def vs.GetWSRowColumnCount(worksheet):
    return (numRows, numColumns)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|numRows|INTEGER|Number of rows in worksheet.|
|numColumns|INTEGER|Number of columns in worksheet.|

## Examples
```pascal
BEGIN
	SearchWorksheet := FALSE;
	IF ((hWS<>NIL) & (GetType(hWS) = 18)) THEN BEGIN
		GetWSRowColumnCount(hWS,rows,cols);{SprdSize(hWS,rows,cols);}
		FOR i := 1 to rows DO BEGIN
			{KID check for a database row with subrows... KID}
			if ( IsWSDatabaseRow( hWS, i ) ) then BEGIN
{				GetWSSubrowCount( hWS, i, subi );

wsHand := GetObject(wsName);
if wsHand <> nil then BEGIN
	if GetType(wsHand) = 18 then BEGIN
		GetWSRowColumnCount(wsHand, numRows, numCols);
		IF numRows < kNumRows THEN InsertWSRows   (wsHand, 1, kNumRows - numRows);
		IF numCols < kNumCols THEN InsertWSColumns(wsHand, 1, kNumCols - numCols);
	end else BEGIN
		while GetObject(wsName) <> nil DO wsName := Concat(wsName, '-1');

BEGIN
	GetWSRowColumnCount (wksHand, rows, cols);
	numClasses := rows - 1;
	FOR i := 1 TO numClasses DO
	BEGIN
		GetWSCellString (wksHand, i+1, 1, tempStr);
```
```python
if ( recHand != 0 ) and ( wksHand != 0 ):
	# * Get the user standard index *
	userIndex = vs.Str2Num( vs.Copy( vs.GetRField( recHand, recName, getLocStr( 12018, 2 ) ), 1, 1 ) )
	rows, cols = vs.GetWSRowColumnCount( wksHand )
	i = 1
	numClasses = rows - 1
	while (i <= numClasses ):
		tempStr = vs.GetWSCellString( wksHand, i + 1, userIndex )
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
