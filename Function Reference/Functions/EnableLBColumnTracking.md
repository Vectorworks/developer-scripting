# EnableLBColumnTracking

## Description
Enables/disables column tracking.

```pascal
PROCEDURE EnableLBColumnTracking(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				columnIndex          : INTEGER;
				enableColumnTracking : BOOLEAN);
```

```python
def vs.EnableLBColumnTracking(dialogID, componentID, columnIndex, enableColumnTracking):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|enableColumnTracking|BOOLEAN|specifies if column tracking should be enabled or disabled|

## Remarks
If reducing column width is allowed or not.

## Examples
```pascal
	boo:=EnableLBSingleLineSelection(dialogIDInventory, kBrowserMain, FALSE);
	EnableLBSorting(dialogIDInventory, kBrowserMain, TRUE);
	IF gNumInst>1 THEN SetLBSortColumn(dialogIDInventory, kBrowserMain, kColType, FALSE);
	EnableLBColumnLines(dialogIDInventory, kBrowserMain, TRUE);
	EnableLBColumnTracking(dialogIDInventory, kBrowserMain, kColType, TRUE);
	RestoreLBColumnWidths('LightingInventorySetup', dialogIDInventory,kBrowserMain);
	EnableItem(dialogIDInventory,kRemoveButton,FALSE);
END;
```
```python
import vs

# Enables/disables column tracking.
dialogID = 1
componentID = 2
columnIndex = 1
enableColumnTracking = True

vs.EnableLBColumnTracking(dialogID, componentID, columnIndex, enableColumnTracking)
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
