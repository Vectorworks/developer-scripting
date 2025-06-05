# SetSprdSortSum

## Description
Procedure SetSprdSortSum specifies sorting and summation options for a database row in the referenced worksheet. For descending sorts, pass the column as a negative value. For no sort, pass 0 as the sumCol column.

```pascal
PROCEDURE SetSprdSortSum(
				sheetHd  : HANDLE;
				row      : INTEGER;
				sortCol1 : INTEGER;
				sortCol2 : INTEGER;
				sortCol3 : INTEGER;
				sumCol   : INTEGER);
```

```python
def vs.SetSprdSortSum(sheetHd, row, sortCol1, sortCol2, sortCol3, sumCol):
    return None
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
Sets sorting and summation for a database row.  The sortCol1, sortCol2, and sortCol3 values specify the primary, secondary and tertiary sorts for the database row.  Pass a positive column for a descending sort; pass a negative column for an ascending sort.  For no sort,  pass 0 as the column.  Sum works the same way. [VML 01/09/01]

## See Also
[SetWSColumnOperators](SetWSColumnOperators.md)

## Version
SetSprdSortSum is obsolete as of VectorWorks 9.0, see new [ SetWSColumnOperators](SetWSColumnOperators.md)

Availability: from VectorWorks 8.0

## Category
* [Worksheets](../Categories/Worksheets.md)
