# GetLineTypeChoice

## Description
Get current choice of line style popup dialog control.  Choice is the internal index (reference number) of the line type.

```pascal
PROCEDURE GetLineTypeChoice(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				VAR lineType : LONGINT);
```

```python
def vs.GetLineTypeChoice(dialogID, itemID):
    return lineType
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the line style control.|
|lineType|LONGINT|The internal index (reference number) of the line type.|

## Examples
```pascal
GetLineTypeChoice( dialogID, MeasureLineStylePop_ID, ChoiceNumber );
convertRes := GetPseudoIndFromDash (ChoiceNumber, pseudoInd);
if NOT convertRes
THEN
	pseudoInd := 2; {for solid line; this case should NEVER happen since we just got ref from popup}

27: BEGIN
	GetLineTypeChoice (dlogID, 27, tempLong);
	gClassList [gClassIndex].LS := tempLong;
	gIsClassAttrsChanged [gClassIndex] := TRUE;
	OK := GetEditInteger (dlogID,27,tempLong);
END;	{of item =27}

GetColorChoice(JoistAttributesDialogID, kFillForePDM, JoistFillFore);
GetColorChoice(JoistAttributesDialogID, kFillBackPDM, 	JoistFillBack);
GetColorChoice(JoistAttributesDialogID, kPenForePDM, JoistPenFore);
GetColorChoice(JoistAttributesDialogID, kPenBackPDM, 	JoistPenBack);
GetLineTypeChoice(JoistAttributesDialogID, kPenLineStylePDM , JoistPenLine);
GetLineWeightChoice(JoistAttributesDialogID, kLineWeightPDM, JoistLineWeight);
GetBooleanItem(JoistAttributesDialogID, kStartCapCB, JoistMapStartCap);
GetBooleanItem(JoistAttributesDialogID, kEndCapCB, JoistMapEndCap);
GetBooleanItem(JoistAttributesDialogID, kRepeatHorizCB, JoistMapHorRepeat);
```
```python
import vs

# Get current choice of line style popup dialog control.
dialogID = 1
itemID = 2

result = vs.GetLineTypeChoice(dialogID, itemID)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
