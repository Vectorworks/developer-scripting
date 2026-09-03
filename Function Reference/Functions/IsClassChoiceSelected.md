# IsClassChoiceSelected

## Description
Returns if 'By Class' is the selected choice in a marker, line style, or color popup control.

```pascal
FUNCTION IsClassChoiceSelected(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.IsClassChoiceSelected(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Id of the dialog|
|componentID|LONGINT|Id of the popup control|

## Examples
```pascal
GetBooleanItem(JoistAttributesDialogID, kStartCapCB, JoistMapStartCap);
GetBooleanItem(JoistAttributesDialogID, kEndCapCB, JoistMapEndCap);
GetBooleanItem(JoistAttributesDialogID, kRepeatHorizCB, JoistMapHorRepeat);
GetBooleanItem(JoistAttributesDialogID, kRepeatVertCB, JoistMapVertRepeat);
JoistLineWeightByClass := IsClassChoiceSelected( JoistAttributesDialogID, kLineWeightPDM );
```
```python
import vs

# Returns if 'By Class' is the selected choice in a marker, line style, or
# color popup control.
dialogID = 1
componentID = 2

ok = vs.IsClassChoiceSelected(dialogID, componentID)
if ok:
    vs.Message('IsClassChoiceSelected succeeded')
else:
    vs.Message('IsClassChoiceSelected failed')
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
