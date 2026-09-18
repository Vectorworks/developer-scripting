# ShowLBItemMkrEditLst

## Description
Indicates if the Edit List option in the popup of the specified list browser item's marker should be shown.

```pascal
PROCEDURE ShowLBItemMkrEditLst(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				showEditList : BOOLEAN);
```

```python
def vs.ShowLBItemMkrEditLst(dialogID, componentID, itemIndex, subItemIndex, showEditList):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|showEditList|BOOLEAN|if the marker's Edit List option is shown in the popup|

## Examples
```pascal
ShowLBItemMkrEditLst(1, 2, 3, 10, TRUE);
```
```python
import vs

# Indicates if the Edit List option in the popup of the specified list
# browser item's marker should be shown.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
showEditList = True

vs.ShowLBItemMkrEditLst(dialogID, componentID, itemIndex, subItemIndex, showEditList)
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
