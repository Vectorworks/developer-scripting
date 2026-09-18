# GetLineWeightChoice

## Description
Get current choice for a line weight dialog control.  The value is in mils.

```pascal
PROCEDURE GetLineWeightChoice(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				VAR lineWeight : INTEGER);
```

```python
def vs.GetLineWeightChoice(dialogID, itemID):
    return lineWeight
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|lineWeight|INTEGER|   |

## Examples
```pascal
OK := GetEditReal(dialog1, kGridMarkerLLEditReal, 3, gGridMarkerLLength);
GetLineWeightChoice(dialog1, kGridMarkerLWPopup, gGridMarkerLWeight);
GetBooleanItem(dialog1, kShowGridLineCheckBox, gShowGridLineExt);
GetSelectedChoiceInfo(dialog1, kCountersignaturePopup, 0, gCountersignChoice, choiceStr);
gCountersignChoice := gCountersignChoice + 1;
{Check for minimum margins}

		26: BEGIN
			GetLineWeightChoice (dlogID, 26, tempInt);
			gClassList [gClassIndex].LW := tempInt;
{
writeln (' gClassIndex = ',gClassIndex,'    gClassList [gClassIndex].LW = ',gClassList [gClassIndex].LW );
}

GetColorChoice(JoistAttributesDialogID, kFillBackPDM, 	JoistFillBack);
GetColorChoice(JoistAttributesDialogID, kPenForePDM, JoistPenFore);
GetColorChoice(JoistAttributesDialogID, kPenBackPDM, 	JoistPenBack);
GetLineTypeChoice(JoistAttributesDialogID, kPenLineStylePDM , JoistPenLine);
GetLineWeightChoice(JoistAttributesDialogID, kLineWeightPDM, JoistLineWeight);
GetBooleanItem(JoistAttributesDialogID, kStartCapCB, JoistMapStartCap);
GetBooleanItem(JoistAttributesDialogID, kEndCapCB, JoistMapEndCap);
GetBooleanItem(JoistAttributesDialogID, kRepeatHorizCB, JoistMapHorRepeat);
GetBooleanItem(JoistAttributesDialogID, kRepeatVertCB, JoistMapVertRepeat);
```
```python
import vs

# Get current choice for a line weight dialog control.
dialogID = 1
itemID = 2

result = vs.GetLineWeightChoice(dialogID, itemID)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
