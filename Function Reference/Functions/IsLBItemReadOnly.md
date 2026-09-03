# IsLBItemReadOnly

## Description
Determines if the specified item is read only.

```pascal
FUNCTION IsLBItemReadOnly(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.IsLBItemReadOnly(dialogID, componentID, itemIndex, subItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row number|
|subItemIndex|INTEGER|the column number|

## Examples
```pascal
resultOK := IsLBItemReadOnly(1, 2, 3, 10);
```
```python
import vs

# Determines if the specified item is read only.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok = vs.IsLBItemReadOnly(dialogID, componentID, itemIndex, subItemIndex)
if ok:
    vs.Message('IsLBItemReadOnly succeeded')
else:
    vs.Message('IsLBItemReadOnly failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
