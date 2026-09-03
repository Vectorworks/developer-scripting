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

## Examples
```pascal
resultOK := SetLBItemGradientOrImageRefNumber(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the specified list browser item's gradient or image.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
refNumber = 3

ok = vs.SetLBItemGradientOrImageRefNumber(dialogID, componentID, itemIndex, subItemIndex, refNumber)
if ok:
    vs.Message('SetLBItemGradientOrImageRefNumber succeeded')
else:
    vs.Message('SetLBItemGradientOrImageRefNumber failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
