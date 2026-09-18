# GetLBItemPenBackColor

## Description
Gets the specified list browser item's pen background color.

```pascal
FUNCTION GetLBItemPenBackColor(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR redIndex   : INTEGER;
				VAR greenIndex : INTEGER;
				VAR blueIndex  : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemPenBackColor(dialogID, componentID, itemIndex, subItemIndex):
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

## Examples
```pascal
resultOK := GetLBItemPenBackColor(1, 2, 3, 10, 5, 1, 2);
```
```python
import vs

# Gets the specified list browser item's pen background color.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, redIndex, greenIndex, blueIndex = vs.GetLBItemPenBackColor(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemPenBackColor returned: ' + str((ok, redIndex, greenIndex, blueIndex)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
