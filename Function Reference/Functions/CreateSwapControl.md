# CreateSwapControl

## Description
Create a swap control within a dialog.  

This control manages multiple overlapping groups of controls, of which a single group of controls is displayed at a time.  The script is able to control which group is displayed based on other data in the dialog.  For example, a dialog may present a scrolling list of items on the left, and a swap control on the right.  As the user selects items in the list, different sets of controls are enabled on the right.  This can be used for a settings (preferences) style dialog or when there are too many choices to use a Tab control effectively.

```pascal
PROCEDURE CreateSwapControl(
				dialogID      : LONGINT;
				swapControlID : LONGINT);
```

```python
def vs.CreateSwapControl(dialogID, swapControlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog.|
|swapControlID|LONGINT|ID of the swap control.|

## Remarks
The swap control is analogous to a tab control, except without the tabs.  Thus, the script switches panes, not the user.

## See Also
VS Functions:
[CreateSwapPane](CreateSwapPane.md) 
| [DisplaySwapPane](DisplaySwapPane.md)

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
