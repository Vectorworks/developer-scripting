# DeleteAllItems

## Description
Deletes all rows from the specified list box.

```pascal
PROCEDURE DeleteAllItems(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.DeleteAllItems(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the list box|

## Examples
```pascal
BEGIN
	DeleteAllItems(dlogID, itemID);
END;

BEGIN
	DeleteAllItems(dialog1, kPopup91);
	FOR i := numSizes DOWNTO 1 DO
		AddChoice(dialog1,  kPopup91,  gSizes[i],  0);
END;

BEGIN
	DeleteAllItems(Dialog,LocDialogItemIndex);
	LocActualItemCount := 0;
	LocPUCount := 0;
	LocIncCounter := 0;
```
```python
import vs

# Deletes all rows from the specified list box.
dialogID = 1
itemID = 2

vs.DeleteAllItems(dialogID, itemID)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
