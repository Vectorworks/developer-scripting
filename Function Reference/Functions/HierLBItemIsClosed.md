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

## Examples
```pascal
resultOK := HierLBItemIsClosed(1, 2, 3);
```
```python
import vs

# Returns whether the indicated container item is closed.
dialogID = 1
componentID = 2
itemIndex = 1

ok = vs.HierLBItemIsClosed(dialogID, componentID, itemIndex)
if ok:
    vs.Message('HierLBItemIsClosed succeeded')
else:
    vs.Message('HierLBItemIsClosed failed')
```

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
