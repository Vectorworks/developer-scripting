# ShowLBItemByClassOpt

## Description
Sets if the specified list browser item's can be edited by the user to select the By Class option.

```pascal
PROCEDURE ShowLBItemByClassOpt(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				isByClassShown : BOOLEAN);
```

```python

def vs.ShowLBItemByClassOpt(dialogID, componentID, itemIndex, subItemIndex, isByClassShown):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|isByClassShown|BOOLEAN|if the item allows the user to pick the By Class option|

## Version
Availability: from Vectorworks 2025.3

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs - Modern - Browser.md)

