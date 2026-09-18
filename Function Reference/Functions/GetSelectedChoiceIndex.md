# GetSelectedChoiceIndex

## Description
Gets the 0-based index of the selected choice.

```pascal
PROCEDURE GetSelectedChoiceIndex(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				startIndex           : INTEGER;
				VAR outSelectedIndex : INTEGER);
```

```python
def vs.GetSelectedChoiceIndex(dialogID, componentID, startIndex):
    return outSelectedIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|startIndex|INTEGER|The index at which to start looking for a selected item.|
|outSelectedIndex|INTEGER|The index of the selected item or -1 if there is no selected item.|

## Examples
```pascal
BEGIN
GetSelectedChoiceIndex(dialogID, slopeDefControlID, 0, tmpSlopeDefIndex);
DisplaySwapPane(dialogID, swapControlID, tmpSlopeDefIndex+1);
gCurrPane 	:= tmpSlopeDefIndex;
END

layerScale := GetLScale( ActLayer );
GetSelectedChoiceIndex(dlogID, kBillowSizeField, 0,billowSizeIndex);
GetSelectedChoiceIndex(dlogID, kBillowVariabilityField, 0,billowVarIndex);
GetBillowRadius(billowSizeIndex, billowVarIndex, rMin, rMax);

BEGIN
	GetSelectedChoiceIndex	(AddEditLegend, kUseSinglePopup, 0, cnt);
	useSingle2D := (cnt = 1) | (cnt = 3);
	useSingle3D := (cnt = 2) | (cnt = 3);
END;
```
```python
import vs

# Gets the 0-based index of the selected choice.
dialogID = 1
componentID = 2
startIndex = 1

result = vs.GetSelectedChoiceIndex(dialogID, componentID, startIndex)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
