# GetColorChoice

## Description
Get current choice for color popup dialog control.

```pascal
PROCEDURE GetColorChoice(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				VAR colorIndex : INTEGER);
```

```python
def vs.GetColorChoice(dialogID, itemID):
    return colorIndex
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
BEGIN
	GetColorChoice(dialogID, kColorPopupID, result);
	gFillColor := result;
	gVectorFillName := '';
	gAislePattern := -1;
	gSelectedClass := '';

BEGIN
gFill_Shapes := TRUE;
GetColorChoice(dialog_ID, 33,temp_Col_1);
GetColorChoice(dialog_ID, 35,temp_Col_2);
colors_changed := NOT((temp_col_1 = gFill_Col_1) & (temp_col_2 = gFill_Col_2));
IF colors_changed THEN
	BEGIN

25: BEGIN
	GetColorChoice (dlogID, 25, gClassList [gClassIndex].PenColor);
	gIsClassAttrsChanged [gClassIndex] := TRUE;
END;
```
```python
import vs

# Get current choice for color popup dialog control.
dialogID = 1
itemID = 2

result = vs.GetColorChoice(dialogID, itemID)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
