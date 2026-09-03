# GetControlData

## Description
Returns information about the specified extended control item.

```pascal
PROCEDURE GetControlData(
				dialogID : LONGINT;
				itemID   : LONGINT;
				VAR data : LONGINT);
```

```python
def vs.GetControlData(dialogID, itemID):
    return data
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index of dialog layout containing the control item.|
|itemID|LONGINT|Index of the control item.|
|data|LONGINT|Current setting of the control.|

## Remarks
This function supports the following control types:
* color button -- the data is a 32-bit number of the red/green/blue components represented as 8-bit numbers
* slider -- the data is the slider position

## Examples
```pascal
IF NOT GetEditReal(dialog_ID, 20, 3, gMin_Size_2) THEN InvalidValue(dialog_ID, 20, item, '');
IF NOT GetEditReal(dialog_ID, 22, 3, gMax_Size_2) THEN InvalidValue(dialog_ID, 22, item, '');
IF NOT GetEditReal(dialog_ID, 24, 1, gMax_Aspect_2) THEN InvalidValue(dialog_ID, 24, item, '');
IF NOT GetEditInteger(dialog_ID, 26, temp_i) THEN InvalidValue(dialog_ID, 26, item, ''); {throw away this value; it is always 100 - gShape_1_pct }
GetControlData(dialog_ID, 30, gDensity);

BEGIN	{//// LiveSliderProc }
	GetControlData( dialogID, ShuttleSlider_ID, SliderData );
	SliderDataAdjusted := (SliderData - kHalfShuttleSliderRange) / kHalfShuttleSliderRange;

1: BEGIN
	GetControlData (dialogID, 5, speed);
END;
```
```python
import vs

# Returns information about the specified extended control item.
dialogID = 1
itemID = 2

result = vs.GetControlData(dialogID, itemID)
```

## See Also
[SetControlData](SetControlData.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
