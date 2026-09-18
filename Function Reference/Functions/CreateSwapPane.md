# CreateSwapPane

## Description
Creates a swap pane within the specified swap control.   Within a swap control, only one swap pane is visible at a time.

```pascal
PROCEDURE CreateSwapPane(
				dialogID      : LONGINT;
				swapControlID : LONGINT;
				newGroupID    : LONGINT);
```

```python
def vs.CreateSwapPane(dialogID, swapControlID, newGroupID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the ID of the dialog|
|swapControlID|LONGINT|the ID of the swap control|
|newGroupID|LONGINT|the ID of the group to be inserted into swap control as a swap pane.|

## Remarks
The function is analogous to CreateTabPane.

## Examples
[ComplexDialogLayout3swap](examples/ComplexDialogLayout3swap.md)

```pascal
BEGIN
	CreateSwapPane (dialogID, 2*i+6, 300+2*i);
	SetFirstGroupItem(dialogID, 300+2*i, 301+2*i);
	CreateSwapPane (dialogID, 2*i+6, 400+2*i);
	SetFirstGroupItem(dialogID, 400+2*i, 401+2*i);
END;

{* Wire controls into swap panes *}
	CreateSwapPane (dialogID, 12, 15);
	SetFirstGroupItem(dialogID, 15, 13);
	CreateSwapPane (dialogID, 12, 16);
	SetFirstGroupItem(dialogID, 16, 14);

CreateSwapPane    (dialogID,  kFillStyleSwapControl, kMainGroupBox);
```
```python
import vs

# Creates a swap pane within the specified swap control.
dialogID = 1
swapControlID = 2
newGroupID = 3

vs.CreateSwapPane(dialogID, swapControlID, newGroupID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[CreateSwapControl](CreateSwapControl.md) 
| [DisplaySwapPane](DisplaySwapPane.md)

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
