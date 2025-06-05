# SetSprdSortSumColumns

## Description
Sets the sorting and summation options for a database row.

```pascal
PROCEDURE SetSprdSortSumColumns(
				sheetHd  : HANDLE;
				row      : INTEGER;
				sortCol1 : INTEGER;
				sortCol2 : INTEGER;
				sortCol3 : INTEGER;
				sumCol1  : INTEGER;
				sumCol2  : INTEGER;
				sumCol3  : INTEGER);
```

```python
def vs.SetSprdSortSumColumns(sheetHd, row, sortCol1, sortCol2, sortCol3, sumCol1, sumCol2, sumCol3):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetHd|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row of worksheet.|
|sortCol1|INTEGER|Primary sort column.|
|sortCol2|INTEGER|Secondary sort column.|
|sortCol3|INTEGER|Tertiary sort column.|
|sumCol1|INTEGER|Primary summation column.|
|sumCol2|INTEGER|Secondary summation column.|
|sumCol3|INTEGER|Tertiary summation column.|

## Remarks
Sets sorting and summation for a database row.  The sortCol1, sortCol2, and sortCol3 values specify the primary, secondary and tertiary sorts for the database row.  Pass a positive column for a descending sort; pass a negative column for an ascending sort.  For no sort,  pass 0 as the column.  Sum works the same way.[VML 01/09/01]

## See Also
[SetWSColumnOperators| SetWSColumnOperators](SetWSColumnOperators|%20SetWSColumnOperators.md)

## Version
SetSprdSortSumColumns is obsolete as of VectorWorks 9.0, see new [ SetWSColumnOperators](SetWSColumnOperators.md)

Availability: from VectorWorks 8.5

## Category
* [Worksheets](../Categories/Worksheets.md)
