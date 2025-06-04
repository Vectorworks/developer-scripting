# SetLBItemGradientOrImageRefNumber

## Description
Sets the specified list browser item's gradient or image.

```pascal
FUNCTION SetLBItemGradientOrImageRefNumber(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				refNumber    : LONGINT): BOOLEAN;
```

```python
def vs.SetLBItemGradientOrImageRefNumber(dialogID, componentID, itemIndex, subItemIndex, refNumber):
    return BOOLEAN
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
