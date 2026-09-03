# SetLBItemByClass

## Description
Sets if the specified list browser item's is by class.

```pascal
PROCEDURE SetLBItemByClass(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				isByClass    : BOOLEAN);
```

```python

def vs.SetLBItemByClass(dialogID, componentID, itemIndex, subItemIndex, isByClass):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|isByClass|BOOLEAN|if the item is by class or not|

## Examples
```pascal
SetLBItemByClass(1, 2, 3, 10, TRUE);
```
```python
import vs

# Sets if the specified list browser item's is by class.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
isByClass = True

ok = vs.SetLBItemByClass(dialogID, componentID, itemIndex, subItemIndex, isByClass)
if ok:
    vs.Message('SetLBItemByClass succeeded')
else:
    vs.Message('SetLBItemByClass failed')
```

## Version
Availability: from Vectorworks 2025.3

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs - Modern - Browser.md)
