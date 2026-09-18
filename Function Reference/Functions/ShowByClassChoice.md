# ShowByClassChoice

## Description
Adds a 'By Class' choice to a marker, line style, or color popup control.  (Dialog must be running)

```pascal
PROCEDURE ShowByClassChoice(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.ShowByClassChoice(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Id of the dialog|
|componentID|LONGINT|Id of the popup control|

## Examples
```pascal
SetColorChoice(JoistAttributesDialogID, kPenForePDM,	JoistPenFore);
SetColorChoice(JoistAttributesDialogID, kPenBackPDM,	JoistPenBack);
SetLineTypeChoice(JoistAttributesDialogID, 	kPenLineStylePDM, 	JoistPenLine   );
SetLineWeightChoice(JoistAttributesDialogID, 	kLineWeightPDM, 	JoistLineWeight);
ShowByClassChoice( JoistAttributesDialogID, kLineWeightPDM );
SelectClassChoice( JoistAttributesDialogID, kLineWeightPDM, JoistLineWeightByClass );
```
```python
import vs

# Adds a 'By Class' choice to a marker, line style, or color popup control.
dialogID = 1
componentID = 2

vs.ShowByClassChoice(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
