# SelectClassChoice

## Description
Use to select the class option in a popup that ShowByClassChoice has been called on.  This function must be called with FALSE param if the popup currently has the class selection and the script wishes to change to a non-class selection.

```pascal
PROCEDURE SelectClassChoice(
				dialogID    : LONGINT;
				componentID : LONGINT;
				select      : BOOLEAN);
```

```python
def vs.SelectClassChoice(dialogID, componentID, select):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Id of the dialog|
|componentID|LONGINT|Id of the popup control|
|select|BOOLEAN|TRUE if setting by class or FALSE if programmatically restoring the value to a non-class setting after class setting was applied|

## Examples
```pascal
SetColorChoice(JoistAttributesDialogID, kPenBackPDM,	JoistPenBack);
SetLineTypeChoice(JoistAttributesDialogID, 	kPenLineStylePDM, 	JoistPenLine   );
SetLineWeightChoice(JoistAttributesDialogID, 	kLineWeightPDM, 	JoistLineWeight);
ShowByClassChoice( JoistAttributesDialogID, kLineWeightPDM );
SelectClassChoice( JoistAttributesDialogID, kLineWeightPDM, JoistLineWeightByClass );
```
```python
import vs

# Use to select the class option in a popup that ShowByClassChoice has been
# called on.
dialogID = 1
componentID = 2
select = True

vs.SelectClassChoice(dialogID, componentID, select)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
