# SetPatternData

## Description
Set current choice and colors for the pattern popup dialog control.

```pascal
PROCEDURE SetPatternData(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				patternIndex : INTEGER;
				foreColor    : INTEGER;
				backColor    : INTEGER);
```

```python
def vs.SetPatternData(dialogID, itemID, patternIndex, foreColor, backColor):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|patternIndex|INTEGER|   |
|foreColor|INTEGER|   |
|backColor|INTEGER|   |

## Examples
```pascal
   fValue := GetRField(gPluginH, GetName(recordHand), 'AislePattern');
IF (fValue <> '-1') THEN BEGIN
	SetPatternData(dialogID, kPatternPopupID,  Str2Num(fValue)  , gBackColor, gForeColor);
	gAislePattern := Str2Num(fValue);
END

SetColorChoice(dlogID,25,gClassList [1].PenColor);
SetLineWeightChoice(dlogID, 26, gClassList [1].LW);
SetLineTypeChoice(dlogID, 27, gClassList [1].LS);
SetPatternData(dlogID,28,gClassList [1].FillPat,gClassList [1].FillFore,gClassList [1].FillBack);
SetColorChoice(dlogID,29,gClassList [1].FillFore);
SetColorChoice(dlogID,30,gClassList [1].FillBack);
SetBooleanItem(dlogID, 31,gClassList [1].UseAtCreation);
SetItemText(dlogID, 13, gClassStdNames [gActClassChoiceI]);
```
```python
import vs

# Set current choice and colors for the pattern popup dialog control.
dialogID = 1
itemID = 2
patternIndex = 1
foreColor = 5
backColor = 5

vs.SetPatternData(dialogID, itemID, patternIndex, foreColor, backColor)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
