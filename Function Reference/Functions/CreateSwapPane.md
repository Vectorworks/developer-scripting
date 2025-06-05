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

## See Also
VS Functions:
[CreateSwapControl](CreateSwapControl.md) 
| [DisplaySwapPane](DisplaySwapPane.md)

## Version
Availability: from VectorWorks11.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
