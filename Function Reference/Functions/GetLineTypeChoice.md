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

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
