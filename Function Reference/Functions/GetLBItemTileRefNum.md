# GetLBItemTileRefNum

## Description
Sets the specified list browser item's tile.

```pascal
FUNCTION GetLBItemTileRefNum(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemIndex     : INTEGER;
				subItemIndex  : INTEGER;
				VAR refNumber : LONGINT): BOOLEAN;
```

```python
def vs.GetLBItemTileRefNum(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, refNumber)
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
resultOK := GetLBItemTileRefNum(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the specified list browser item's tile.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, refNumber = vs.GetLBItemTileRefNum(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemTileRefNum returned: ' + str((ok, refNumber)))
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
