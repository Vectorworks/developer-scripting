# IsWSSubrowCellString

## Description
Returns whether a specified database subrow cell contains a numeric value.

```pascal
FUNCTION IsWSSubrowCellString(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				subrow    : INTEGER): BOOLEAN;
```

```python
def vs.IsWSSubrowCellString(worksheet, row, column, subrow):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
|subrow|INTEGER|Index of subrow to be queried.|

## Remarks
Determines if the specified worksheet subrow cell's contents is a string value.
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk

## Examples
```pascal
{				GetWSSubrowCount( hWS, i, subi );
				For k := 1 to subi DO
					FOR j := 1 to cols DO BEGIN
						IF ( IsValidWSSubrowCell(hWS,i,j,k) ) THEN
							if ( IsWSSubrowCellString (hWS,i,j,k) ) then BEGIN
								GetWSSubrowCellString ( hWS, i, j, k, cellStr );
								{process sub row cell - not possible to change the cell value
								without changing the field it has been got from!!!}
{							END;{of if}
{					END;{of for}
```
```python
import vs

# Returns whether a specified database subrow cell contains a numeric value.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5
subrow = 10

ok = vs.IsWSSubrowCellString(worksheet, row, column, subrow)
if ok:
    vs.Message('IsWSSubrowCellString succeeded')
else:
    vs.Message('IsWSSubrowCellString failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
