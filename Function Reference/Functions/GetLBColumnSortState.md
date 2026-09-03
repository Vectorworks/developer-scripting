# GetLBColumnSortState

## Description
Gets the column sort state. Returns 0: not sorted; -1: 1..n sorted; 1: n..1 sorted.

```pascal
FUNCTION GetLBColumnSortState(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): INTEGER;
```

```python
def vs.GetLBColumnSortState(dialogID, componentID, columnIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|

## Examples
```pascal
	BEGIN
		SaveDialogPosition('ChooseSchedule', dlogID);
	END;
1, -5: BEGIN
		sortState := GetLBColumnSortState(dlogID, 5, 0);
		schedIndex := -1;
		LB_GetSelChoice(dlogID, 5, 0, schedIndex, schedFile);

BEGIN
	isAscending := ( GetLBColumnSortState(AddEditLegend, kFieldsLB, kColNumber) < 0 );
	gNumRows := GetNumLBItems(AddEditLegend, kFieldsLB);
	FOR cnt := 0 to gNumRows-1 DO
	BEGIN
		IF isAscending THEN
```
```python
import vs

# Gets the column sort state.
dialogID = 1
componentID = 2
columnIndex = 1

resultN = vs.GetLBColumnSortState(dialogID, componentID, columnIndex)
vs.Message('GetLBColumnSortState returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
