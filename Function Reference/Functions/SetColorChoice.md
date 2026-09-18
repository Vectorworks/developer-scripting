# SetColorChoice

## Description
Sets the choice for the color popup dialog control to the specified color index.

```pascal
PROCEDURE SetColorChoice(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				colorIndex : INTEGER);
```

```python
def vs.SetColorChoice(dialogID, itemID, colorIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|colorIndex|INTEGER|   |

## Examples
[ColorPopupDialog](examples/ColorPopupDialog.md)

```pascal
if gForeColor <> 0 then
	SetColorChoice(dialogID, kForeColorPopupID, gForeColor)
else
begin
    gForeColor := 257;
    SetColorChoice(dialogID, kForeColorPopupID, gForeColor);
end;

seteditinteger(dialog_ID,44,gDensity);
SetBooleanItem(dialog_ID, 31, gFill_Shapes);
gFill_Col_1 := ColorVar2Index(g__Fill_RGB_1);
gFill_Col_2 := ColorVar2Index(g__Fill_RGB_2);
SetColorChoice(dialog_ID,33,gFill_Col_1);
SetColorChoice(dialog_ID,35,gFill_Col_2);
SetBooleanItem(dialog_ID, 36, gUse_Fade);
SetEditReal(dialog_ID, 38, 1, gFade_Depth);
SetBooleanItem(dialog_ID, 41, gRandom_Rotate);

SetColorChoice(dlogID,25,gClassList [1].PenColor);
SetLineWeightChoice(dlogID, 26, gClassList [1].LW);
SetLineTypeChoice(dlogID, 27, gClassList [1].LS);
SetPatternData(dlogID,28,gClassList [1].FillPat,gClassList [1].FillFore,gClassList [1].FillBack);
SetColorChoice(dlogID,29,gClassList [1].FillFore);
```
```python
import vs

# Sets the choice for the color popup dialog control to the specified color
# index.
dialogID = 1
itemID = 2
colorIndex = 1

vs.SetColorChoice(dialogID, itemID, colorIndex)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
