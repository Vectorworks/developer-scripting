# GetActivePane

## Description
Returns the currently displayed tab or swap pane in the specified tab or swap control.

This is called from the dialog's event handling routine.

```pascal
FUNCTION GetActivePane(
				dialogID     : LONGINT;
				tabControlID : LONGINT): LONGINT;
```

```python
def vs.GetActivePane(dialogID, tabControlID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the ID of the dialog|
|tabControlID|LONGINT|the ID of the swap control|

## Remarks
Note that pane indeces are 1-based in VectorScript, and 0-based in the SDK.  Panes are numbered sequentially in the order that they were inserted into the control.  This applies to both tab and swap controls

This doesn't return the control ID per se, but rather, the sequential number of the tab or swap pane, in the order in which it was added to the tab/swap control (1, 2, 3, etc.).

## Examples


## See Also
VS Functions:
[CreateSwapControl](CreateSwapControl.md) 
| [CreateSwapPane](CreateSwapPane.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
