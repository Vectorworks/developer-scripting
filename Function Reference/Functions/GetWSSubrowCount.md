# GetWSSubrowCount

## Description
Returns a count of displayed subrows for a specified database row.

```pascal
PROCEDURE GetWSSubrowCount(
				worksheet      : HANDLE;
				databaseRow    : INTEGER;
				VAR numSubrows : INTEGER);
```

```python
def vs.GetWSSubrowCount(worksheet, databaseRow):
    return numSubrows
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaseRow|INTEGER|Database row to be queried.|
|numSubrows|INTEGER|Number of displayed subrows.|

## Remarks
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk.

(*\_c\_*, 2014.09.25): This fails returning zero numSubrows -or other wrong values- when the worksheet needs recalculation: use [RecalculateWS](RecalculateWS.md) before calling for the count of subrows.

([[User:Juliancarr|Julian]], 2018.05.22): If you call this in a script that is being executed via the Runscript command in a worksheet, it will return the current row number that is being processed. This allows the script to access data from database rows by using [GetWSSubrowCellValue](GetWSSubrowCellValue.md).

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
