# GetEditReal

## Description
Returns the numeric value from the specified REAL numeric edit field control.

```pascal
FUNCTION GetEditReal(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				editRealType : LONGINT;
				VAR value    : REAL): BOOLEAN;
```

```python
def vs.GetEditReal(dialogID, itemID, editRealType):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|editRealType|LONGINT|The type of REAL value being returned.|
|value|REAL|The value contained in the field.|

## Remarks
does math, handles units, returns false for any error in conversion. For an explanation of editRealType, see the CreateEditReal call

## Examples
#### VectorScript ####
```pascal
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);

PROCEDURE InvalidValue(controlID :INTEGER);
BEGIN
item := -1;
SelField(controlID);
SysBeep;
END;

BEGIN
CASE item OF
SetupDialogC: SetEditReal(dialogID, 11, 3, elevation);
1: IF NOT(GetEditReal(dialogID, 11, 3, elevation)) 
THEN InvalidValue(11);
END;
END;
```
#### Python ####
```python

```

```pascal
	END;
1:	BEGIN { user selected OK button }
	if (not GetEditInteger(dlogID,8,numRows)) | (numRows < 1) then InvalidValue(dlogID, 8, item, '') ELSE
	if (not GetEditInteger(dlogID,9,numCols)) | (numCols < 1) then InvalidValue(dlogID, 9, item, '') ELSE
	IF (NOT GetEditReal(dlogID,10,3,gridFreq)) | (NOT (gridFreq > 0)) THEN InvalidValue(dlogID, 10, item, '');
	finished := (item = 1);
	END;

GetSelectedChoiceInfo(IDLabelDialog, kLabelShape, 0, DWBubbleIndex , DWBubble);
LocalBubbleToUni;
boo := GetEditReal(IDLabelDialog,kBubbleSize,3,DWBubbleSize);
GetSelectedChoiceInfo(IDLabelDialog, kLabelClass, 0, I, DWClass);
GetLineTypeAttriData(IDLabelDialog,kIDLeaderLS,DWLineStyle,DWLineWeight);
GetLineTypeAttriData(IDLabelDialog,kBubbleLS,BubbleLS,BubbleLW);
            GetMarkerValue(IDLabelDialog,kLeaderStyle, DWMarkerStyle, MarkerAngle, MarkerSize, MarkerWidth, MarkerBasis, MarkerThickness );

BEGIN
	boolD := GetEditReal(dlgId, kHeightEdit, 3, dHeightTotal);
	IF (dHeightTotal > pFloorThk * nFloors) AND (bAllowFloor = FALSE) THEN
	BEGIN
		FOR i:=1 TO nFloors DO
		BEGIN
```
```python
result = vs.GetEditReal(dialogID, itemID, editRealType)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
