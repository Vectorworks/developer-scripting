# IsWSDatabaseRow

## Description
Returns whether a row in the referenced worksheet is a database row.

```pascal
FUNCTION IsWSDatabaseRow(
				worksheet   : HANDLE;
				databaseRow : INTEGER): BOOLEAN;
```

```python
def vs.IsWSDatabaseRow(worksheet, databaseRow):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Row to be queried.|

## Examples
```pascal
	IF ((hWS<>NIL) & (GetType(hWS) = 18)) THEN BEGIN
		GetWSRowColumnCount(hWS,rows,cols);{SprdSize(hWS,rows,cols);}
		FOR i := 1 to rows DO BEGIN
			{KID check for a database row with subrows... KID}
			if ( IsWSDatabaseRow( hWS, i ) ) then BEGIN
{				GetWSSubrowCount( hWS, i, subi );
				For k := 1 to subi DO
					FOR j := 1 to cols DO BEGIN
						IF ( IsValidWSSubrowCell(hWS,i,j,k) ) THEN
							if ( IsWSSubrowCellString (hWS,i,j,k) ) then BEGIN
```
```python
import vs

# Returns whether a row in the referenced worksheet is a database row.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaseRow = 10

ok = vs.IsWSDatabaseRow(worksheet, databaseRow)
if ok:
    vs.Message('IsWSDatabaseRow succeeded')
else:
    vs.Message('IsWSDatabaseRow failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
