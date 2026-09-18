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

## Examples
```pascal
	SetWSCellBorder(wsHand, kTitleRow,   kLocCol, kTitleRow, kNumCols,   FALSE, FALSE, FALSE, FALSE, TRUE);
	SetWSCellBorder(wsHand, kFldNameRow, kLocCol, kNumRows,  kRadiusCol, TRUE,  TRUE,  TRUE,  TRUE,  TRUE);
	str := Concat('=DATABASE(INOBJECT & (R IN [''NNA_PropertyLine_CurveData''])) & (L=', QStr(GetLName(GetLayer(objHand))), ')');
	SetWSCellFormula(wsHand, kNumRows, 0, kNumRows, 0, str);
	SetWSColumnOperators(wsHand, kNumRows, -1, 0, 0, 0, 0, 0);
	RecalculateWS(wsHand);
END;

SetWSCellFormula(tempHandle,1,1,1,1,GetPlugInString(5004)); {nominal}
SetWSCellTextFormat(tempHandle,1,2,1,2,fontIndex,10,1);
SetWSCellFormula(tempHandle,1,2,1,2,GetPlugInString(5005)); {count}
SetWSCellFormula(tempHandle,2,0,2,0,'=DATABASE((R IN [''FramingMember'']))');
SetWSColumnOperators(tempHandle,2,-1,0,0,1,0,0);
SetWSCellFormula(tempHandle,2,1,2,1,'=(''FramingMember''.quantityLabel)');
SetWSCellFormula(tempHandle,2,2,2,2,'1');
ShowWS(tempHandle,TRUE);	{Show WS}
RecalculateWS( tempHandle );

{add a summation item}
SetWSColumnOperators(tempHandle, numHeadings + 2, 1, 0, 0, 0, 0, 0);
```
```python
import vs

# Sets sort and summarize column operators for a database row in the
# referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
sort1 = 1
sort2 = 2
sort3 = 3
sum1 = 10
sum2 = 1
sum3 = 2

vs.SetWSColumnOperators(worksheet, row, sort1, sort2, sort3, sum1, sum2, sum3)
```
See also in tutorials: [26. Sorting and Grouping with `SetWSColumnOperators`](ai%20examples/26_WorksheetSortAndGroup.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
