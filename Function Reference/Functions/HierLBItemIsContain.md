# HierLBItemIsContain

## Description
Returns whether the indicated item is a container item.

```pascal
FUNCTION HierLBItemIsContain(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER): BOOLEAN;
```

```python
def vs.HierLBItemIsContain(dialogID, componentID, itemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog containing the list browser.|
|componentID|LONGINT|The ID of the list browser.|
|itemIndex|INTEGER|The index of the item.|

## Examples
```pascal
resultOK := HierLBItemIsContain(1, 2, 3);
```
```python
import vs

# Returns whether the indicated item is a container item.
dialogID = 1
componentID = 2
itemIndex = 1

ok = vs.HierLBItemIsContain(dialogID, componentID, itemIndex)
if ok:
    vs.Message('HierLBItemIsContain succeeded')
else:
    vs.Message('HierLBItemIsContain failed')
```

## See Also
VS Functions:
[HierLBItemIsClosed](HierLBItemIsClosed.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
