# GetWSColumnOperators

## Description
Returns the sort and summarize column operators for a database row in the referenced worksheet.

```pascal
PROCEDURE GetWSColumnOperators(
				worksheet : HANDLE;
				row       : INTEGER;
				VAR sort1 : INTEGER;
				VAR sort2 : INTEGER;
				VAR sort3 : INTEGER;
				VAR sum1  : INTEGER;
				VAR sum2  : INTEGER;
				VAR sum3  : INTEGER);
```

```python
def vs.GetWSColumnOperators(worksheet, row):
    return (sort1, sort2, sort3, sum1, sum2, sum3)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row to be queried.|
|sort1|INTEGER|Primary sort column.|
|sort2|INTEGER|Secondary sort column.|
|sort3|INTEGER|Tertiary sort column.|
|sum1|INTEGER|Primary summarize column.|
|sum2|INTEGER|Secondary summarize column.|
|sum3|INTEGER|Tertiary summarize column.|

## Examples
```pascal
GetWSColumnOperators(worksheet, 1, 2, 3, 10, 5, 1, 2);
```
```python
import vs

# Returns the sort and summarize column operators for a database row in the
# referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10

sort1, sort2, sort3, sum1, sum2, sum3 = vs.GetWSColumnOperators(worksheet, row)
vs.Message('GetWSColumnOperators returned: ' + str((sort1, sort2, sort3, sum1, sum2, sum3)))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
