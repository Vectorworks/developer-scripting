# HierLBItemOpened

## Description
This function is called when the user clicks on a container item to open it. It wil redisplay items inside the container that were hidden (unless they are inside a lower level container that is closed), but only with the hierarchical name set. If other data needs to be redisplayed, it will need to be done with other functions. numbRedisplItems indicates how many non-container items were redisplayed.

```pascal
PROCEDURE HierLBItemOpened(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				itemIndex            : INTEGER;
				recursive            : BOOLEAN;
				VAR numbRedisplItems : INTEGER);
```

```python
def vs.HierLBItemOpened(dialogID, componentID, itemIndex, recursive):
    return numbRedisplItems
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog containing the list browser.|
|componentID|LONGINT|The id of the list browser.|
|itemIndex|INTEGER|The index of the item that was clicked on.|
|recursive|BOOLEAN|Indicates whether any subcontainers should also be opened.|
|numbRedisplItems|INTEGER|The number of items that were redisplayed.|

## See Also
VS Functions:
[HierLBItemClosed](HierLBItemClosed.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
