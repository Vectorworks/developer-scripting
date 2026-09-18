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

## Examples
```pascal
SelectChoice(IDLabelDialog, kLabelShape, DWBubbleIndex, TRUE);
SetLineTypeAttriData(IDLabelDialog,kIDLeaderLS,DWLineStyle,DWLineWeight);
SetLineTypeAttriData(IDLabelDialog,kBubbleLS,BubbleLS,BubbleLW);
SetBooleanItem(IDLabelDialog, kShowLeader,DWShowLeader);
SetBooleanItem(IDLabelDialog, kUseMarker,UseMarker);
SetBooleanItem(IDLabelDialog, kAutoRotate,DWHorz);
```
```python
import vs

# Set current choices for the line attribute dialog control.
dialogID = 1
itemID = 2
lineType = 0
lineWeight = 3

vs.SetLineTypeAttriData(dialogID, itemID, lineType, lineWeight)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
