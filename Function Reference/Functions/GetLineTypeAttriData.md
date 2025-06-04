# GetLineTypeAttriData

## Description
Get the current choices for the combined line style and line weight dialog control.  The line type value is the line type internal index (reference number). The line weight value is in mils.

```pascal
PROCEDURE GetLineTypeAttriData(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				VAR lineType   : LONGINT;
				VAR lineWeight : INTEGER);
```

```python
def vs.GetLineTypeAttriData(dialogID, itemID):
    return (lineType, lineWeight)
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
