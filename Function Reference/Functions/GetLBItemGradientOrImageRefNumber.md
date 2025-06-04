# GetLBItemGradientOrImageRefNumber

## Description
Gets the specified list browser item's gradient or image.

```pascal
FUNCTION GetLBItemGradientOrImageRefNumber(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemIndex     : INTEGER;
				subItemIndex  : INTEGER;
				VAR refNumber : LONGINT): BOOLEAN;
```

```python
def vs.GetLBItemGradientOrImageRefNumber(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, refNumber)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|refNumber|LONGINT|the gradient or image's ref number|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
