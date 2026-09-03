# SetLineTypeChoice

## Description
Set the current choice of the line style popup dialog control to the specified line type.

```pascal
PROCEDURE SetLineTypeChoice(
				dialogID : LONGINT;
				itemID   : LONGINT;
				lineType : LONGINT);
```

```python
def vs.SetLineTypeChoice(dialogID, itemID, lineType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the line style control.|
|lineType|LONGINT|The internal index (reference number) of the line type.|

## Examples
```pascal
	BEGIN
		lineStyle := CheckLSN(-1); {set to basic dash line if valid value not found}
	END;
	SetLineTypeChoice( dialogID, MeasureLineStylePop_ID, lineStyle );
END

SetColorChoice(dlogID,25,gClassList [1].PenColor);
SetLineWeightChoice(dlogID, 26, gClassList [1].LW);
SetLineTypeChoice(dlogID, 27, gClassList [1].LS);
SetPatternData(dlogID,28,gClassList [1].FillPat,gClassList [1].FillFore,gClassList [1].FillBack);
SetColorChoice(dlogID,29,gClassList [1].FillFore);
SetColorChoice(dlogID,30,gClassList [1].FillBack);
SetBooleanItem(dlogID, 31,gClassList [1].UseAtCreation);

SetColorChoice(JoistAttributesDialogID, kFillForePDM,	JoistFillFore);
SetColorChoice(JoistAttributesDialogID, kFillBackPDM,	JoistFillBack);
SetColorChoice(JoistAttributesDialogID, kPenForePDM,	JoistPenFore);
SetColorChoice(JoistAttributesDialogID, kPenBackPDM,	JoistPenBack);
SetLineTypeChoice(JoistAttributesDialogID, 	kPenLineStylePDM, 	JoistPenLine   );
SetLineWeightChoice(JoistAttributesDialogID, 	kLineWeightPDM, 	JoistLineWeight);
ShowByClassChoice( JoistAttributesDialogID, kLineWeightPDM );
SelectClassChoice( JoistAttributesDialogID, kLineWeightPDM, JoistLineWeightByClass );
```
```python
import vs

# Set the current choice of the line style popup dialog control to the
# specified line type.
dialogID = 1
itemID = 2
lineType = 0

vs.SetLineTypeChoice(dialogID, itemID, lineType)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
