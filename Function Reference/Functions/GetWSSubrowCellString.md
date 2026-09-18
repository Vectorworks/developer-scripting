# GetWSSubrowCellString

## Description
Returns the displayed string in a database subrow cell.

```pascal
PROCEDURE GetWSSubrowCellString(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				subrow         : INTEGER;
				VAR cellString : STRING);
```

```python
def vs.GetWSSubrowCellString(worksheet, row, column, subrow):
    return cellString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
|subrow|INTEGER|Index of subrow cell to be queried.|
|cellString|STRING|Display string of subrow cell.|

## Remarks
Gets the specified worksheet subrow cell's displayed string.
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk.

## Examples
```pascal
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

# Returns the displayed string in a database subrow cell.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5
subrow = 10

text = vs.GetWSSubrowCellString(worksheet, row, column, subrow)
vs.Message('GetWSSubrowCellString returned: ' + str(text))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
