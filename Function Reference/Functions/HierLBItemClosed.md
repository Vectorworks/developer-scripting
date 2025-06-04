# HierLBItemClosed

## Description
This function is called when the user clicks on a container item to close it. It will remove items that are inside the container being closed.

```pascal
PROCEDURE HierLBItemClosed(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER;
				recursive   : BOOLEAN);
```

```python
def vs.HierLBItemClosed(dialogID, componentID, itemIndex, recursive):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog containing the list browser.|
|componentID|LONGINT|The id of the list browser.|
|itemIndex|INTEGER|The index of the item that was clicked on.|
|recursive|BOOLEAN|Whether to also close any containers inside the container that was clicked on.|

## See Also
VS Functions:
[HierLBItemOpened](HierLBItemOpened.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
