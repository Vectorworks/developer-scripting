# SetLBItemTileRefNum

## Description
Sets the specified list browser item's tile.

```pascal
FUNCTION SetLBItemTileRefNum(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				refNumber    : LONGINT): BOOLEAN;
```

```python
def vs.SetLBItemTileRefNum(dialogID, componentID, itemIndex, subItemIndex, refNumber):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the colum index|
|refNumber|LONGINT|the tile's ref number|

## Examples
```pascal
resultOK := SetLBItemTileRefNum(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the specified list browser item's tile.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
refNumber = 3

ok = vs.SetLBItemTileRefNum(dialogID, componentID, itemIndex, subItemIndex, refNumber)
if ok:
    vs.Message('SetLBItemTileRefNum succeeded')
else:
    vs.Message('SetLBItemTileRefNum failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
