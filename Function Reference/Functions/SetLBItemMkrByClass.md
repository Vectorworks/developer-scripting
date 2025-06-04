# SetLBItemMkrByClass

## Description
Sets if the specified list browser item's marker is by class.

```pascal
FUNCTION SetLBItemMkrByClass(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				isByClass    : BOOLEAN): BOOLEAN;
```

```python
def vs.SetLBItemMkrByClass(dialogID, componentID, itemIndex, subItemIndex, isByClass):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|isByClass|BOOLEAN|if the marker is by class or not|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
