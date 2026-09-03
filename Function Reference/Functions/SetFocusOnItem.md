# SetFocusOnItem

## Description
Sets the keyboard input focus on the specified item.

```pascal
PROCEDURE SetFocusOnItem(
				liDialogID    : LONGINT;
				liComponentID : LONGINT);
```

```python
def vs.SetFocusOnItem(liDialogID, liComponentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |

## Examples
```pascal
SetFocusOnItem(CablePickerDialog, kOK);

3:	BEGIN
		SetBooleanItem(Dialog, kSelectByFieldValBtn, TRUE);
		EnableItem(Dialog, kFieldNamePopUp, TRUE);
		EnableItem(Dialog, kFieldValEditBx, TRUE);
		SetFocusOnItem(Dialog, kFieldValEditBx);
	END;
```
```python
import vs

# Sets the keyboard input focus on the specified item.
liDialogID = 1
liComponentID = 2

vs.SetFocusOnItem(liDialogID, liComponentID)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
