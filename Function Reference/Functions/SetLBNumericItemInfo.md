# SetLBNumericItemInfo

## Description
Sets numeric data for item.

```pascal
FUNCTION SetLBNumericItemInfo(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				itemString   : STRING;
				itemNumVal   : REAL;
				imageIndex   : INTEGER): BOOLEAN;
```

```python
def vs.SetLBNumericItemInfo(dialogID, componentID, itemIndex, subItemIndex, itemString, itemNumVal, imageIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog that contains the list browser.|
|componentID|LONGINT|ID of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the subitem index|
|itemString|STRING|the item text|
|itemNumVal|REAL|the item numeric value|
|imageIndex|INTEGER|the item image list index|

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
