# HierLBItemIsClosed

## Description
Returns whether the indicated container item is closed.

```pascal
FUNCTION HierLBItemIsClosed(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER): BOOLEAN;
```

```python
def vs.HierLBItemIsClosed(dialogID, componentID, itemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|
|itemIndex|INTEGER|The index of the item.|

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
