# GetLBItemByClass

## Description
Gets if the specified list browser item's is by class.

```pascal
FUNCTION GetLBItemByClass(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER) : BOOLEAN;
```

```python

def vs.GetLBItemByClass(dialogID, componentID, itemIndex, subItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|

## Returns
Returns whether the specified list browser item is set, or not, to be by class.

## Version
Availability: from Vectorworks 2025.3

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs - Modern - Browser.md)

