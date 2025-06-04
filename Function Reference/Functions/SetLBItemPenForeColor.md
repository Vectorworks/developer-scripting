# SetLBItemPenForeColor

## Description
Sets the specified list browser item's pen foreground color.

```pascal
FUNCTION SetLBItemPenForeColor(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				redIndex     : INTEGER;
				greenIndex   : INTEGER;
				blueIndex    : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemPenForeColor(dialogID, componentID, itemIndex, subItemIndex, redIndex, greenIndex, blueIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|redIndex|INTEGER|the red component (0 - 255)|
|greenIndex|INTEGER|the green component (0 - 255)|
|blueIndex|INTEGER|the blue component (0 - 255)|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
