# SetControlData

## Description
Sets the data for the specified extended control item. 

This function can only be called from within the dialog event handler subroutine.

```pascal
PROCEDURE SetControlData(
				dialogID : LONGINT;
				itemID   : LONGINT;
				data     : LONGINT);
```

```python
def vs.SetControlData(dialogID, itemID, data):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog containing the control.|
|itemID|LONGINT|The index of the dialog control item.|
|data|LONGINT|New data for the control item.|

## Remarks
This function supports the following control types:
* color button -- the data is a 32-bit number of the red/green/blue components represented as 8-bit numbers
* slider -- the data is the slider position
* image -- the data is the ID of the image resource being displayed.

## Examples
```pascal
SetEditReal(dialog_ID, 20, 3, gMin_Size_2);
SetEditReal(dialog_ID, 22, 3, gMax_Size_2);
SetEditReal(dialog_ID, 24, 1, gMax_Aspect_2);
SetEditInteger(dialog_ID, 26, (100 - gShape_1_pct));
SetControlData(dialog_ID, 30, gDensity);
seteditinteger(dialog_ID,44,gDensity);
SetBooleanItem(dialog_ID, 31, gFill_Shapes);
gFill_Col_1 := ColorVar2Index(g__Fill_RGB_1);
gFill_Col_2 := ColorVar2Index(g__Fill_RGB_2);

BEGIN
	SetControlData( dialogID, ShuttleSlider_ID, kHalfShuttleSliderRange );
	SliderDataAdjusted := (SliderData - kHalfShuttleSliderRange) / kHalfShuttleSliderRange;

BEGIN
	CASE item OF
		SetUpDialogC: BEGIN
			SetControlData (dialogID, 5, speed);
		END;
```
```python
import vs

# Sets the data for the specified extended control item.
dialogID = 1
itemID = 2
data = 3

vs.SetControlData(dialogID, itemID, data)
```

## See Also
[GetControlData](GetControlData.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
