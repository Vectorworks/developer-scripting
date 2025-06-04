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

## See Also
[GetWSRowColumnCount| GetWSRowColumnCount](GetWSRowColumnCount|%20GetWSRowColumnCount.md)

## Version
SprdSize is obsolete as of VectorWorks 9.0, see new [[VS:GetWSRowColumnCount| GetWSRowColumnCount]].

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
