# SetLineWeightChoice

## Description
Set the current choice of the line weight dialog control to the value specified in mils.

```pascal
PROCEDURE SetLineWeightChoice(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				lineWeight : INTEGER);
```

```python
def vs.SetLineWeightChoice(dialogID, itemID, lineWeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|lineWeight|INTEGER|   |

## Examples
```pascal
SetLineWeightChoice(dialog1, kGridMarkerLWPopup, gGridMarkerLWeight);
SetEditReal(dialog1, kGridMarkerLLEditReal, 3, gGridMarkerLLength);
SetBooleanItem(dialog1, kShowGridLineCheckBox, gShowGridLineExt);
FOR i := gCountersignCnt DOWNTO 1 DO
	AddChoice(dialog1,  kCountersignaturePopup,  gCountersignArray [i, 2],  0);

SetColorChoice(dlogID,25,gClassList [1].PenColor);
SetLineWeightChoice(dlogID, 26, gClassList [1].LW);
SetLineTypeChoice(dlogID, 27, gClassList [1].LS);
SetPatternData(dlogID,28,gClassList [1].FillPat,gClassList [1].FillFore,gClassList [1].FillBack);
SetColorChoice(dlogID,29,gClassList [1].FillFore);
SetColorChoice(dlogID,30,gClassList [1].FillBack);

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

# Set the current choice of the line weight dialog control to the value
# specified in mils.
dialogID = 1
itemID = 2
lineWeight = 3

vs.SetLineWeightChoice(dialogID, itemID, lineWeight)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
