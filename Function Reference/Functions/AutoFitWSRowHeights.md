# AutoFitWSRowHeights

## Description
Auto fit the height of rows to the content of the cells in the referenced worksheet.

AutoFitWSRowHeights allows height for a range of rows to be auto fitted to the contents of cells. To auto fit the height of a single worksheet row, specify identical values for the top/bottom row range boundaries.

```pascal
PROCEDURE AutoFitWSRowHeights(
				worksheet : HANDLE;
				fromRow   : INTEGER;
				toRow     : INTEGER);
```

```python
def vs.AutoFitWSRowHeights(worksheet, fromRow, toRow):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|fromRow|INTEGER|Top row of row range|
|toRow|INTEGER|Bottom row of row range|

## Examples
#### VectorScript ####
```pascal
{Auto resizes the height of all rows from row 1 to row 4} 
PROCEDURE Example;
VAR
sheet :HANDLE;
BEGIN
sheet := GetTopVisibleWS; 
AutoFitWSRowHeights(sheet,1,4);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	sheet = vs.GetTopVisibleWS() 
	vs.AutoFitWSRowHeights(sheet,1,4)
Example()
```

```pascal
AutoFitWSRowHeights(worksheet, 1, 2);
```
```python
import vs

# Auto fit the height of rows to the content of the cells in the referenced
# worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
fromRow = 10
toRow = 10

vs.AutoFitWSRowHeights(worksheet, fromRow, toRow)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
