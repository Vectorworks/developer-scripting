# GetSprdSortSum

## Description
Procedure GetSprdSortSum returns sorting and summation options for a database row in the referenced worksheet.

```pascal
PROCEDURE GetSprdSortSum(
				sheetHd      : HANDLE;
				row          : INTEGER;
				VAR sortCol1 : INTEGER;
				VAR sortCol2 : INTEGER;
				VAR sortCol3 : INTEGER;
				VAR sumCol   : INTEGER);
```

```python
def vs.GetSprdSortSum(sheetHd, row):
    return (sortCol1, sortCol2, sortCol3, sumCol)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetHd|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet database row index.|
|sortCol1|INTEGER|Primary sort column index.|
|sortCol2|INTEGER|Secondary sort column index.|
|sortCol3|INTEGER|Tertiary sort column index.|
|sumCol|INTEGER|Summation column.|

## Remarks
Gets sorting for a database row.  The sortCol1, sortCol2, and sortCol3 values specify the primary, secondary and tertiary sorts for the database row.  For descending sorts, a positive column is returned; for ascending sorts, a negative column is returned.  For no sort,  0 is returned. Sum works the same way. [VML 01/09/01]

## Examples
```pascal
GetSprdSortSum(sheetHd, 1, 2, 3, 10, 5);
```
```python
import vs

# Procedure GetSprdSortSum returns sorting and summation options for a
# database row in the referenced worksheet.
sheetHd = vs.FSActLayer()  # handle to the first selected object on the active layer
row = 10

sortCol1, sortCol2, sortCol3, sumCol = vs.GetSprdSortSum(sheetHd, row)
vs.Message('GetSprdSortSum returned: ' + str((sortCol1, sortCol2, sortCol3, sumCol)))
```

## See Also
[GetWSColumnOperators](GetWSColumnOperators.md)

## Version
GetSprdSortSum is obsolete as of VectorWorks 9.0, see new [GetWSColumnOperators](GetWSColumnOperators.md).

Availability: from VectorWorks 8.0

## Category
* [Worksheets](../Categories/Worksheets.md)
