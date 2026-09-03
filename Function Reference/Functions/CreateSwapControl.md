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

## Examples
```pascal
BEGIN
	fieldNum := n1 + i - 1;
	CreateCheckBox (dialogID, 2*i+5, '');
	CreateStaticText (dialogID, 600+2*i, fieldName [fieldNum], labelWidth);
	CreateSwapControl (dialogID, 2*i+6);
	CreateGroupBox    (dialogID, 300+2*i, '', TRUE);
	CreateEditText    (dialogID, 301+2*i, '', 45);
	CreateGroupBox    (dialogID, 400+2*i, '', TRUE);
	CreatePullDownMenu(dialogID, 401+2*i, 45);

CreatePullDownMenu (dialogID, 8, 32);
CreateStaticText (dialogID, 9, GetPlugInString (3021), labelWidth);
CreatePullDownMenu (dialogID, 10, 32);
CreateStaticText (dialogID, 11, GetPlugInString (3022), labelWidth);
CreateSwapControl (dialogID, 12);
CreateGroupBox    (dialogID, 15, '', TRUE);
CreateEditText    (dialogID, 13, '', 32);
CreateGroupBox    (dialogID, 16, '', TRUE);
CreatePullDownMenu(dialogID, 14, 32);

CreateGroupBox    (dialogID,  kFirstGroupBox, '', False);
CreateSwapControl (dialogID,  kFillStyleSwapControl);
```
```python
import vs

# Create a swap control within a dialog.
dialogID = 1
swapControlID = 2

vs.CreateSwapControl(dialogID, swapControlID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[CreateSwapPane](CreateSwapPane.md) 
| [DisplaySwapPane](DisplaySwapPane.md)

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
