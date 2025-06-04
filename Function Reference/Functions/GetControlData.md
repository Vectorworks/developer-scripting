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

## See Also
[SetControlData](SetControlData.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
