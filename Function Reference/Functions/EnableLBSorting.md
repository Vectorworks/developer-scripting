# EnableLBSorting

## Description
Enables/disables sorting.

```pascal
PROCEDURE EnableLBSorting(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				enableSorting : BOOLEAN);
```

```python
def vs.EnableLBSorting(dialogID, componentID, enableSorting):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enableSorting|BOOLEAN|specifies whether to enable or disable sorting|

## Examples
```pascal
EnableLBSorting(dlgId, kLBCtrl, FALSE);
{EnableLBColumnLines(dlgId, kLBCtrl, TRUE);} {enables direct edit}
boolD := EnableLBSingleLineSelection(dlgId, kLBCtrl, TRUE);

	EnableLBSorting(dlogID, itemID, FALSE);
	EnableLBColumnLines(dlogID, itemID, TRUE);
	tempRes := EnableLBSingleLineSelection(dlogID, itemID, TRUE);
END;

BEGIN
	EnableLBSorting(dlogID, 5, TRUE);
	IF isMac THEN
		lbColumn := InsertLBColumn(dlogID, 5, 0, GetPluginString(4004), 263)
	ELSE
		lbColumn := InsertLBColumn(dlogID, 5, 0, GetPluginString(4004), 236);
```
```python
import vs

# Enables/disables sorting.
dialogID = 1
componentID = 2
enableSorting = True

vs.EnableLBSorting(dialogID, componentID, enableSorting)
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
