# GetSprdSortSumColumns

## Description
Returns the sorting and summation options for a database row.

```pascal
PROCEDURE GetSprdSortSumColumns(
				sheetHd      : HANDLE;
				row          : INTEGER;
				VAR sortCol1 : INTEGER;
				VAR sortCol2 : INTEGER;
				VAR sortCol3 : INTEGER;
				VAR sumCol1  : INTEGER;
				VAR sumCol2  : INTEGER;
				VAR sumCol3  : INTEGER);
```

```python
def vs.GetSprdSortSumColumns(sheetHd, row):
    return (sortCol1, sortCol2, sortCol3, sumCol1, sumCol2, sumCol3)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetHd|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row to be queried.|
|sortCol1|INTEGER|Primary sort column.|
|sortCol2|INTEGER|Secondary sort column.|
|sortCol3|INTEGER|Tertiary sort column.|
|sumCol1|INTEGER|Primary summation column.|
|sumCol2|INTEGER|Secondary summation column.|
|sumCol3|INTEGER|Tertiary summation column.|

## Remarks
Gets sorting for a database row.  The sortCol1, sortCol2, and sortCol3 values specify the primary, secondary and tertiary sorts for the database row.  For descending sorts, a positive column is returned; for ascending sorts, a negative column is returned  For no sort,  0 is returned.  Sum works the same way.
OBSOLETE for Version 9: see new GetWSColumnOperators. [VML 01/09/01]

## Version
GetSprdSortSumColumns is obsolete as of VectorWorks9.0<P>


Availability: from VectorWorks8.5

## Category
* [Worksheets](../Categories/Worksheets.md)
