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

## See Also
[GetControlData](GetControlData.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
