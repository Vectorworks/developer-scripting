# GetLBItemFillForeColor

## Description
Gets the specified list browser item's fill foreground color.

```pascal
FUNCTION GetLBItemFillForeColor(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR redIndex   : INTEGER;
				VAR greenIndex : INTEGER;
				VAR blueIndex  : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemFillForeColor(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, redIndex, greenIndex, blueIndex)
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
