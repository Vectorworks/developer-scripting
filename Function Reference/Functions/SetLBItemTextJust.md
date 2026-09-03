# SetLBItemTextJust

## Description
Sets the text alignment for the specified list browser item.

```pascal
FUNCTION SetLBItemTextJust(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemIndex     : INTEGER;
				subItemIndex  : INTEGER;
				justification : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextJust(dialogID, componentID, itemIndex, subItemIndex, justification):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|justification|INTEGER|Left - 1|Center - 2|Right - 3|

## Examples
```pascal
	boolD := SetLBItemInfo(dlgId, kLBCtrl, nFloors, colId1,  clNameLast, -1);{}
	boolD := SetLBItemTextJust(dlgId, kLBCtrl, nFloors, colId1 , 1);{1-left, 2-right, 3-center}
	boolD := SetLBItemInteracType(dlgId, kLBCtrl,nFloors, colId1, 4);{kListBrowserItemInteractionEditClass}
{Elevation}
	boolD := SetLBItemInfo(dlgId, kLBCtrl, nFloors, colId2, num2strF( Str2Num( elevNameLast ) + Str2Num( flHeightNameLast ) ), 0);
	boolD := SetLBItemTextJust(dlgId, kLBCtrl, nFloors, colId2 , 3);{1-left, 2-right, 3-center}
```
```python
import vs

# Sets the text alignment for the specified list browser item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
justification = 3

ok = vs.SetLBItemTextJust(dialogID, componentID, itemIndex, subItemIndex, justification)
if ok:
    vs.Message('SetLBItemTextJust succeeded')
else:
    vs.Message('SetLBItemTextJust failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
