# SetLBItemFillBackColor

## Description
Sets the specified list browser item's fill background color.

```pascal
FUNCTION SetLBItemFillBackColor(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				redIndex     : INTEGER;
				greenIndex   : INTEGER;
				blueIndex    : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemFillBackColor(dialogID, componentID, itemIndex, subItemIndex, redIndex, greenIndex, blueIndex):
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

## Examples
[SetLBItemPatternIndex](SetLBItemPatternIndex.md)

```pascal
			Red := ((TempColorArray [RowCount+1].Red))/257;
			Green := ((TempColorArray [RowCount+1].Green))/257;
			Blue := ((TempColorArray [RowCount+1].Blue))/257;
			bFlipTexture := SetLBColumnOwnerDrawnType( dialog, kFrntMltColBrowser, RowCount,2,1);
			bFlipTexture := SetLBItemFillBackColor( dialog, kFrntMltColBrowser, RowCount,2,Red,Green,Blue);
			bFlipTexture := SetLBItemFillForeColor( dialog, kFrntMltColBrowser, RowCount,2,Red,Green,Blue);
{This line caused crash:  IF IsUserColor(ColorIndexForName,ColorName) then Begin End;}
```
```python
import vs

# Sets the specified list browser item's fill background color.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
redIndex = 1
greenIndex = 1
blueIndex = 1

ok = vs.SetLBItemFillBackColor(dialogID, componentID, itemIndex, subItemIndex, redIndex, greenIndex, blueIndex)
if ok:
    vs.Message('SetLBItemFillBackColor succeeded')
else:
    vs.Message('SetLBItemFillBackColor failed')
```

## See Also
[SetLBItemFillForeColor](SetLBItemFillForeColor.md) | [SetLBItemFillBackColor](SetLBItemFillBackColor.md)

[SetLBControlType](SetLBControlType.md) | [SetLBItemDisplayType](SetLBItemDisplayType.md) | [SetLBColumnOwnerDrawnType](SetLBColumnOwnerDrawnType.md) | [SetLBItemPatternIndex](SetLBItemPatternIndex.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
