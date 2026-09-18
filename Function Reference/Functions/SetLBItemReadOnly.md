# SetLBItemReadOnly

## Description
Sets the item's read-only state.

```pascal
PROCEDURE SetLBItemReadOnly(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				readOnly     : BOOLEAN);
```

```python
def vs.SetLBItemReadOnly(dialogID, componentID, itemIndex, subItemIndex, readOnly):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|readOnly|BOOLEAN|the read-only state|

## Examples
```pascal
SetLBItemReadOnly(1, 2, 3, 10, TRUE);
```
```python
import vs

# Sets the item's read-only state.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
readOnly = True

vs.SetLBItemReadOnly(dialogID, componentID, itemIndex, subItemIndex, readOnly)
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
