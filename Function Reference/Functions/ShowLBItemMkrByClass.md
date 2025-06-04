# ShowLBItemMkrByClass

## Description
Indicates if the By Class option in the popup of the specified list browser item's marker should be shown.

```pascal
PROCEDURE ShowLBItemMkrByClass(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				showByClass  : BOOLEAN);
```

```python
def vs.ShowLBItemMkrByClass(dialogID, componentID, itemIndex, subItemIndex, showByClass):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|showByClass|BOOLEAN|if the marker's By Class option is shown in the popup|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
