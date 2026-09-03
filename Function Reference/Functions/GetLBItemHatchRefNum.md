# GetLBItemHatchRefNum

## Description
Sets the specified list browser item's hatch.

```pascal
FUNCTION GetLBItemHatchRefNum(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemIndex     : INTEGER;
				subItemIndex  : INTEGER;
				VAR refNumber : LONGINT): BOOLEAN;
```

```python
def vs.GetLBItemHatchRefNum(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, refNumber)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the colum index|
|refNumber|LONGINT|the hatch's ref number|

## Examples
```pascal
resultOK := GetLBItemHatchRefNum(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the specified list browser item's hatch.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, refNumber = vs.GetLBItemHatchRefNum(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemHatchRefNum returned: ' + str((ok, refNumber)))
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
