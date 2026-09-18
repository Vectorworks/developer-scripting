# SetLayoutDialogSize

## Description
Sets a Layout Manager dialog's size, in pixels.

```pascal
PROCEDURE SetLayoutDialogSize(
				dialogID : LONGINT;
				width    : INTEGER;
				height   : INTEGER);
```

```python
def vs.SetLayoutDialogSize(dialogID, width, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|width|INTEGER|   |
|height|INTEGER|   |

## Examples
```pascal
IF GetSavedSetting('DialogPositions', Concat(dialogName, '/hght'), value)	THEN
	hght := Str2Int(value)	ELSE hght := 0;
if (left > 0) & (top > 0) then BEGIN
	{Don't do this is position is null.}
	SetLayoutDialogSize(dialogID, wdth, hght);
	boo := SetLayoutDialogPosition(dialogID, left, top);

SetLayoutDialogSize(dialogID, wdth, hght);

BEGIN
{Don't do this is position is null.}
SetLayoutDialogSize(dialogID, wdth, hght);
boo := SetLayoutDialogPosition(dialogID, left, top);
END;
```
```python
import vs

# Sets a Layout Manager dialog's size, in pixels.
dialogID = 1
width = 2
height = 3

vs.SetLayoutDialogSize(dialogID, width, height)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
