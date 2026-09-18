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

## Examples
```pascal
	boolD := SetLBItemInfo(dlgId, kLBCtrl, nFloors, colId1,  clNameLast, -1);{}
	boolD := SetLBItemTextJust(dlgId, kLBCtrl, nFloors, colId1 , 1);{1-left, 2-right, 3-center}
	boolD := SetLBItemInteracType(dlgId, kLBCtrl,nFloors, colId1, 4);{kListBrowserItemInteractionEditClass}
{Elevation}
	boolD := SetLBItemInfo(dlgId, kLBCtrl, nFloors, colId2, num2strF( Str2Num( elevNameLast ) + Str2Num( flHeightNameLast ) ), 0);
	boolD := SetLBItemTextJust(dlgId, kLBCtrl, nFloors, colId2 , 3);{1-left, 2-right, 3-center}
	boolD := SetLBItemInteracType(dlgId, kLBCtrl,nFloors, colId2, 1);
```
```python
import vs

# Sets interaction type for item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
interactionType = 0

ok = vs.SetLBItemInteracType(dialogID, componentID, itemIndex, subItemIndex, interactionType)
if ok:
    vs.Message('SetLBItemInteracType succeeded')
else:
    vs.Message('SetLBItemInteracType failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
