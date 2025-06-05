# DisplayTabPane

## Description
Causes the specified swap pane to be displayed within the specified swap control. 

This is called from the dialog's event handling routine.

```pascal
PROCEDURE DisplayTabPane(
				dialogID     : LONGINT;
				tabControlID : LONGINT;
				groupNumber  : LONGINT);
```

```python
def vs.DisplayTabPane(dialogID, tabControlID, groupNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the ID of the dialog|
|tabControlID|LONGINT|the ID of the swap control|
|groupNumber|LONGINT|1-based index of the swap pane to be displayed|

## Remarks
Note that pane indeces are 1-based in VectorScript, and 0-based in the SDK.  Tab panes are numbered sequentially in the order that they were inserted into the control.

## Examples
[ComplexDialogLayout6](examples/ComplexDialogLayout6.md)

## See Also
VS Functions:
[CreateSwapControl](CreateSwapControl.md) 
| [CreateSwapPane](CreateSwapPane.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
