# SetEditInteger

## Description
Sets the numeric value of the specified INTEGER numeric edit field control.

```pascal
PROCEDURE SetEditInteger(
				dialogID : LONGINT;
				itemID   : LONGINT;
				value    : LONGINT);
```

```python
def vs.SetEditInteger(dialogID, itemID, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|value|LONGINT|The new value for the field.|

## Examples
```pascal
SetupDialogC: BEGIN
	numRows := p__numRows;
	numCols := p__numCols;
	gridFreq := p__gridFreq;
	SetEditInteger (dlogID,8,numRows);
	SetEditInteger (dlogID,9,numCols);
	SetEditReal (dlogID,10,3,gridFreq);
	SelectEditText(dlogID, 8);

{Init controls data here}
SetEditReal( dlgId, kHeightEdit, 3, pHeight );
SetEditInteger( dlgId, kFloorCountEdit, pNumFloors );
SetBooleanItem( dlgId, kAllowIndividualCheck, pAllowFloor );
SetBooleanItem( dlgId, kSetSlabCheck, pSlabEqualsHeight );

BEGIN
SetEditInteger(dialogID, ndx2DlogID2(cnt), Str2Num(GetRField(objHand, objName, flds[cnt].uniName)));
END;
```
```python
import vs

# Sets the numeric value of the specified INTEGER numeric edit field control.
dialogID = 1
itemID = 2
value = 3

vs.SetEditInteger(dialogID, itemID, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
