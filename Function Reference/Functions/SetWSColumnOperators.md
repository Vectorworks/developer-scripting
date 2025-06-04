# SetWSColumnOperators

## Description
Sets sort and summarize column operators for a database row in the referenced worksheet.

```pascal
PROCEDURE SetWSColumnOperators(
				worksheet : HANDLE;
				row       : INTEGER;
				sort1     : INTEGER;
				sort2     : INTEGER;
				sort3     : INTEGER;
				sum1      : INTEGER;
				sum2      : INTEGER;
				sum3      : INTEGER);
```

```python
def vs.SetWSColumnOperators(worksheet, row, sort1, sort2, sort3, sum1, sum2, sum3):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row that will be assigned new sort/summarize operators.|
|sort1|INTEGER|Primary sort column.|
|sort2|INTEGER|Secondary sort column.|
|sort3|INTEGER|Tertiary sort column.|
|sum1|INTEGER|Primary summarize column.|
|sum2|INTEGER|Secondary summarize column.|
|sum3|INTEGER|Tertiary summarize column.|

## Remarks
This by default sets sorting always to descending. In order to set sorting to ascending, use a negative column index (from Bill Wood, in the VS-list).

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
