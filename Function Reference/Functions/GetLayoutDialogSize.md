# GetLayoutDialogSize

## Description
Retrieves a Layout Manager dialog's size, in pixels.

```pascal
PROCEDURE GetLayoutDialogSize(
				dialogID   : LONGINT;
				VAR width  : INTEGER;
				VAR height : INTEGER);
```

```python
def vs.GetLayoutDialogSize(dialogID):
    return (width, height)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|width|INTEGER|   |
|height|INTEGER|   |

## Examples
```pascal
BEGIN
	boo := GetLayoutDialogPosition(dialogID, left, top, right, bottom);
	IF left < 1 THEN left := 1;
	IF top < 1 THEN top := 1;
	GetLayoutDialogSize(dialogID, wdth, hght);
	SetSavedSetting('DialogPositions', Concat(dialogName, '/left'), Int2Str(left));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/top'), Int2Str(top));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/wdth'), Int2Str(wdth));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/hght'), Int2Str(hght));

GetLayoutDialogSize(dialogID, wdth, hght);

BEGIN
	boo := GetLayoutDialogPosition(dialogID, left, top, right, bottom);
	IF left < 1 THEN left := 1;
	IF top < 1 THEN top := 1;
	GetLayoutDialogSize(dialogID, wdth, hght);
	SetSavedSetting('DialogPositions', Concat(dialogName, '/left'), Concat(left));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/top'), Concat(top));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/wdth'), Concat(wdth));
	SetSavedSetting('DialogPositions', Concat(dialogName, '/hght'), Concat(hght));
```
```python
import vs

# Retrieves a Layout Manager dialog's size, in pixels.
dialogID = 1

width, height = vs.GetLayoutDialogSize(dialogID)
vs.Message('GetLayoutDialogSize returned: ' + str((width, height)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
