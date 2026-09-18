# IsWSCellString

## Description
Determines if a cell in the referenced worksheet contains a string value. The cell is referenced by its row-column position in the worksheet.

```pascal
FUNCTION IsWSCellString(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER): BOOLEAN;
```

```python
def vs.IsWSCellString(worksheet, row, column):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|

## Examples
```pascal
{					END;{of for}
			end else BEGIN
				{check each string cell for the string}
				FOR j := 1 to cols DO BEGIN
					if ( IsWSCellString(hWS,i,j) ) then BEGIN
						GetWSCellString( hWS, i, j, cellStr );
						IF ( FindString( cellStr ,gFindString,1,gCase) > 0 )
							then IF ( ProcessFoundCell( hWS, i, j, cellStr ) ) then BEGIN
								SearchWorksheet := TRUE;
								GOTO 98;

SchedFound := TRUE;
GetWSCellString(WSHand,2, ColNum,gPrintedSchedName);
GetWSCellString(WSHand,3, ColNum,gHeaderFont);
{Check if it is V10}
	IF IsWSCellString(WSHand,4, ColNum) THEN
		BEGIN
		GetWSCellString(WSHand,4, ColNum,TempS);
		gHeaderStyle := 1;
			BEGIN
			IF TempS = GetLocStr(15018,10) THEN gHeaderStyle := 0
				ELSE IF TempS = GetLocStr(15018,11) THEN gHeaderStyle := 1
```
```python
import vs

# Determines if a cell in the referenced worksheet contains a string value.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5

ok = vs.IsWSCellString(worksheet, row, column)
if ok:
    vs.Message('IsWSCellString succeeded')
else:
    vs.Message('IsWSCellString failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
