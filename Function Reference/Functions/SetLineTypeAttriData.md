# SetLineTypeAttriData

## Description
Set current choices for the line attribute dialog control.  Both the line type and the line weight in mils can be specified.

```pascal
PROCEDURE SetLineTypeAttriData(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				lineType   : LONGINT;
				lineWeight : INTEGER);
```

```python
def vs.SetLineTypeAttriData(dialogID, itemID, lineType, lineWeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the line attribute control.|
|lineType|LONGINT|The internal index (reference number) of the line type.|
|lineWeight|INTEGER|The line weight.The value is in mils.|

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
