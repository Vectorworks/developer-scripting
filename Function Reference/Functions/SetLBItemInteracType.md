# SetLBItemInteracType

## Description
Sets interaction type for item.

```pascal
FUNCTION SetLBItemInteracType(
				dialogID        : LONGINT;
				componentID     : LONGINT;
				itemIndex       : INTEGER;
				subItemIndex    : INTEGER;
				interactionType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemInteracType(dialogID, componentID, itemIndex, subItemIndex, interactionType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the subitem index|
|interactionType|INTEGER|the interaction type|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
