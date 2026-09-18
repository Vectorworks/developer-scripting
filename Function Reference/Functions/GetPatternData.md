# GetPatternData

## Description
Get current choice for pattern popup dialog control, and the displayed foreground and background color indexes.

```pascal
PROCEDURE GetPatternData(
				dialogID         : LONGINT;
				itemID           : LONGINT;
				VAR patternIndex : INTEGER;
				VAR foreColor    : INTEGER;
				VAR backColor    : INTEGER);
```

```python
def vs.GetPatternData(dialogID, itemID):
    return (patternIndex, foreColor, backColor)
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
BEGIN
	GetPatternData(dialogID, kPatternPopupID,  index, gForeColor, gBackColor);
	GetColorChoice(dialogID, kForeColorPopupID, gForeColor);
	GetColorChoice(dialogID, kBackColorPopupID, gBackColor);

		28: BEGIN
			GetPatternData(dlogID,28,gClassList [gClassIndex].FillPat,gClassList [gClassIndex].FillFore,gClassList [gClassIndex].FillBack);
			gIsClassAttrsChanged [gClassIndex] := TRUE;
{
writeln (' ########### gClassIndex = ',gClassIndex,'    FillPat = ',gClassList [gClassIndex].FillPat);
}

GetPatternData(JoistAttributesDialogID, kFillPatternPDM,  JoistFillPattern, JoistFillFore, JoistFillBack);
GetPatternData(JoistAttributesDialogID, kPenPatternPDM,  JoistPenPattern, JoistPenFore, JoistPenBack );
GetColorChoice(JoistAttributesDialogID, kFillColorPDM, JoistFillColor);
GetColorChoice(JoistAttributesDialogID, kPenColorPDM, 	JoistPenColor	);
GetColorChoice(JoistAttributesDialogID, kFillForePDM, JoistFillFore);
```
```python
import vs

# Get current choice for pattern popup dialog control, and the displayed
# foreground and background color indexes.
dialogID = 1
itemID = 2

patternIndex, foreColor, backColor = vs.GetPatternData(dialogID, itemID)
vs.Message('GetPatternData returned: ' + str((patternIndex, foreColor, backColor)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
