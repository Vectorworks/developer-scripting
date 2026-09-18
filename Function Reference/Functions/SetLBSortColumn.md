# SetLBSortColumn

## Description
Sets the specified column as the sort column in the specified list browser control.

```pascal
PROCEDURE SetLBSortColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				isAscending : BOOLEAN);
```

```python
def vs.SetLBSortColumn(dialogID, componentID, columnIndex, isAscending):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|
|isAscending|BOOLEAN|determines if the sort should be ascending or descending|

## Examples
```pascal
	IF isMac THEN
		lbColumn := InsertLBColumn(dlogID, 5, 0, GetPluginString(4004), 263)
	ELSE
		lbColumn := InsertLBColumn(dlogID, 5, 0, GetPluginString(4004), 236);
	SetLBSortColumn(dlogID, 5, 0, TRUE);
END;

LDevice_DlgResource( AddEditLegend, kSelSymResource, gSelectedSymbolName );
{Initialize the rows to be used in kFieldsLB.}
EnableLBColumnLines(AddEditLegend, kFieldsLB, TRUE);
SetLBSortColumn(AddEditLegend, kFieldsLB, kColNumber, FALSE);

	{//////// Set LB Options ////////}
	boo:=EnableLBSingleLineSelection(dialogIDIM, kBrowser, FALSE);
	EnableLBSorting(dialogIDIM, kBrowser, TRUE);
	IF GetNumLBItems(dialogIDIM, kBrowser)>1 THEN SetLBSortColumn(dialogIDIM, kBrowser, 0, FALSE);
	EnableLBColumnLines(dialogIDIM, kBrowser, TRUE);
	EnableLBHierDisplay(dialogIDIM, kBrowser, FALSE);
	RestoreLBColumnWidths('Dlg_Inst_Mnt', dialogIDIM,kBrowser);
END;
```
```python
import vs

# Sets the specified column as the sort column in the specified list browser
# control.
dialogID = 1
componentID = 2
columnIndex = 1
isAscending = True

vs.SetLBSortColumn(dialogID, componentID, columnIndex, isAscending)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
