# DisplaySwapPane

## Description
Causes the specified swap pane to be displayed within the specified swap control. 

This is called from the dialog's event handling routine.

```pascal
PROCEDURE DisplaySwapPane(
				dialogID      : LONGINT;
				swapControlID : LONGINT;
				groupNumber   : LONGINT);
```

```python
def vs.DisplaySwapPane(dialogID, swapControlID, groupNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the ID of the dialog|
|swapControlID|LONGINT|the ID of the swap control|
|groupNumber|LONGINT|1-based index of the swap pane to be displayed|

## Remarks
Note that pane indeces are 1-based in VectorScript, and 0-based in the SDK.  Swap panes are numbered sequentially in the order that they were inserted into the control.

Counter-intuitively, groupNumber is not the index of the groupbox that you want displayed, but rather, a 1-based index which is dynamically incremented every time you call CreateSwapPane. So if you want to display whatever you put into the first call of CreateSwapPane, then call [DisplaySwapPane](DisplaySwapPane.md) with an index of 1.

## Examples
[ComplexDialogLayout5](examples/ComplexDialogLayout5.md)

```pascal
BEGIN
	loadPopupChoices (gCurrentDialogID, pulldownID, fieldName [fieldNum], gNewValue [fieldNum]);
	DisplaySwapPane (gCurrentDialogID, swapControlID, 2);
	EnableItem(gCurrentDialogID, pulldownID, gChangeField [fieldNum]);
END

		RemoveChoice (dialogID, 14, 0);
	FOR i := 1 TO gNumPopupValues DO
		AddChoice (dialogID, 14, popupValues [i], i - 1);
	SelectChoice (dialogID, 14, 0, TRUE);
	DisplaySwapPane (dialogID, 12, 2);
END

fValue := GetRField(gPluginH, GetName(recordHand), 'filling');
SelectChoice(dialogID, kFillStylePopupID, Str2Num(fValue), TRUE);
DisplaySwapPane(dialogID, kFillStyleSwapControl, Str2Num(fValue)+1);
```
```python
import vs

# Causes the specified swap pane to be displayed within the specified swap
# control.
dialogID = 1
swapControlID = 2
groupNumber = 3

vs.DisplaySwapPane(dialogID, swapControlID, groupNumber)
```

## See Also
VS Functions:
[CreateSwapControl](CreateSwapControl.md) 
| [CreateSwapPane](CreateSwapPane.md)

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
