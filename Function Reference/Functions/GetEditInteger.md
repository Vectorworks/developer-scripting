# GetEditInteger

## Description
Returns the numeric value from the specified INTEGER numeric edit field control.

```pascal
FUNCTION GetEditInteger(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				VAR value : LONGINT): BOOLEAN;
```

```python
def vs.GetEditInteger(dialogID, itemID):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|value|LONGINT|The value contained in the field.|

## Remarks
does math, returns false for any error in conversion

## Examples
```pascal
	END;
1:	BEGIN { user selected OK button }
	if (not GetEditInteger(dlogID,8,numRows)) | (numRows < 1) then InvalidValue(dlogID, 8, item, '') ELSE
	if (not GetEditInteger(dlogID,9,numCols)) | (numCols < 1) then InvalidValue(dlogID, 9, item, '') ELSE
	IF (NOT GetEditReal(dlogID,10,3,gridFreq)) | (NOT (gridFreq > 0)) THEN InvalidValue(dlogID, 10, item, '');
	finished := (item = 1);
	END;

BEGIN
	boolD := GetEditInteger(dlgId, kFloorCountEdit, nFloorCount);

BEGIN
IF GetEditInteger(dialogID, ndx2DlogID2(cnt), num)
	THEN str := Num2Str(0, num)
	ELSE InvalidValue(dialogID, ndx2DlogID2(cnt), item, '');
END;
```
```python
import vs

# Returns the numeric value from the specified INTEGER numeric edit field
# control.
dialogID = 1
itemID = 2

ok, value = vs.GetEditInteger(dialogID, itemID)
vs.Message('GetEditInteger returned: ' + str((ok, value)))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
