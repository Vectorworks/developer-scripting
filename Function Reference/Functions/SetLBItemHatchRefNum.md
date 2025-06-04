# SetLBItemHatchRefNum

## Description
Sets the specified list browser item's hatch.

```pascal
FUNCTION SetLBItemHatchRefNum(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				refNumber    : LONGINT): BOOLEAN;
```

```python
def vs.SetLBItemHatchRefNum(dialogID, componentID, itemIndex, subItemIndex, refNumber):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|refNumber|LONGINT|the hatch's ref number|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
