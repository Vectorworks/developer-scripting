# GetCellNum

## Description
Function GetCellNum returns the numeric value of a cell in the referenced worksheet.

```pascal
FUNCTION GetCellNum(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): REAL;
```

```python
def vs.GetCellNum(h, row, col):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## Examples
```pascal
BEGIN
	numPoints := GetCellNum (wksH, 1, 2);

BEGIN
	numRows := GetCellNum (wksH, 1, 2);
	IF numRows > 0 THEN
	BEGIN
		getData := TRUE;

GetWSCellValue (wksH, 3, 2, supportTypeL);
xLeft := GetCellNum (wksH, 4, 2);
```
```python
import vs

# Function GetCellNum returns the numeric value of a cell in the referenced
# worksheet.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
row = 10
col = 5

value = vs.GetCellNum(h, row, col)
vs.Message('GetCellNum returned: ' + str(value))
```

## See Also
[GetWSCellValue](GetWSCellValue.md), [GetWSSubrowCellValue](GetWSSubrowCellValue.md)

## Version
GetCellNum is obsolete as of VectorWorks 9.0, see new [ GetWSCellValue](GetWSCellValue.md) and [ GetWSSubrowCellValue](GetWSSubrowCellValue.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
