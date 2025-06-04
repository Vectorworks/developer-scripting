# SetLBItemTextStyle

## Description
Sets the text style for the specified list browser item.

```pascal
FUNCTION SetLBItemTextStyle(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				textStyle    : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextStyle(dialogID, componentID, itemIndex, subItemIndex, textStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|textStyle|INTEGER|Plain - 0|Bold - 1|Italic - 2|Underline - 4|Outline - 16 (Mac only)|Shadow - 32 (Mac only)|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
