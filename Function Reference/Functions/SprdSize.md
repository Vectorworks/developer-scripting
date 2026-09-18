# SprdSize

## Description
Procedure SprdSize returns the number of rows and columns in the referenced worksheet.

```pascal
PROCEDURE SprdSize(
				h       : HANDLE;
				VAR row : INTEGER;
				VAR col : INTEGER);
```

```python
def vs.SprdSize(h):
    return (row, col)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Returns row size of worksheet.|
|col|INTEGER|Returns column size of worksheet.|

## Examples
```pascal
SprdSize (wksH2, nRows, nCols);
SetWSCellFormula (wksH2, gIndex_Data + r0 + 1, 1, nRows, nCols, '');

{* Check the size to make sure there are enough rows *}
SprdSize (wksH2, nRows, nCols);
IF nRows < numGridPoints + 5 THEN
BEGIN
	InsertWSRows (wksH2, nRows, numGridPoints + 5 - nRows);
	SetWSCellNumberFormat(wksH2, nRows - 1, 1, numGridPoints + 5, 6, 13, 0, '', '');
```
```python
import vs

# Procedure SprdSize returns the number of rows and columns in the referenced
# worksheet.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

row, col = vs.SprdSize(h)
vs.Message('SprdSize returned: ' + str((row, col)))
```

## See Also
[GetWSRowColumnCount](GetWSRowColumnCount.md)

## Version
SprdSize is obsolete as of VectorWorks 9.0, see new [ GetWSRowColumnCount](GetWSRowColumnCount.md).

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
