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

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
