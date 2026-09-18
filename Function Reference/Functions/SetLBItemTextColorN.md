# SetLBItemTextColorN

## Description
Sets the text color tint for the specified list browser item.

```pascal
FUNCTION SetLBItemTextColorN(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				tint         : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextColorN(dialogID, componentID, itemIndex, subItemIndex, tint):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|tint|INTEGER|Tint number. See Appendix for the available values.|

## Remarks
For a list of available tints, see [SetStaticTextColorN](SetStaticTextColorN.md)

## Examples
```pascal
BEGIN
	boo:=SetLBItemTextColorN(dialogIDIM, kBrowser, row, kCandlePowerCol, kTouchedTintVal);
	{Store the values set by the tint so we an find the tinted row later}
	boo:=GetLBItemTextColor(dialogIDIM, kBrowser, row, kCandlePowerCol, TintR, TintG, TintB);
	END;
```
```python
import vs

# Sets the text color tint for the specified list browser item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
tint = 3

ok = vs.SetLBItemTextColorN(dialogID, componentID, itemIndex, subItemIndex, tint)
if ok:
    vs.Message('SetLBItemTextColorN succeeded')
else:
    vs.Message('SetLBItemTextColorN failed')
```

## Version
Availability: from Vectorworks 2023

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
