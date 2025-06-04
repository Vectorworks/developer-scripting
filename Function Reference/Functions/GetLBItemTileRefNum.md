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

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
