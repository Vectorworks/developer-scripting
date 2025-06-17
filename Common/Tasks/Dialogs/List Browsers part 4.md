For better understanding please use the comprehensive example at [Dialog with List Browser](./Dialog%20with%20List%20Browser.md).

By --\_c\_  03:08, 31 December 2020 (EST), previously Orso B. Schmid.

| [Part 1: Creation](./List%20Browsers%20part%201.md) | [Part 2: Columns](./List%20Browsers%20part%202.md) | [Part 3: Rows and Cells](./List%20Browsers%20part%203.md) | [Part 4: Events](./List%20Browsers%20part%204.md) |

# Events

List Browsers can return an event on user's click or mouse activity through [GetLBEventInfo](../../../Function%20Reference/Functions/GetLBEventInfo.md), see examples below. The list of list browser's events is to be found in the SDK in the file `SDKLib/Include/Kernel/MiniCadCallbacks.X.h`.

[GetLBEventInfo](../../../Function%20Reference/Functions/GetLBEventInfo.md) returns a set of three informations:

- row selected
- column selected
- event triggered

```pascal
{ list browser events }
kLBrowColDataSel = -2;	{ user changed column data items, this occurs also without click }
kLBDataChangeAllClick	= -3; {}
kLBrowSel = -4;	{ user clicked on row }
kLBDoubleClick = -5; { I can't ever get this to show, must be SDK only }
kLBDeleteKeyPressed	= -6;
kLBUpKeyPressed	 = -7;
kLBDownKeyPressed = -8; { user scrolled a row using arrow keys: no rows and cols are set by GetLBEventInfo }
kLBAlphaNumericKeyPressed = -9; { user typed a key and the LB scrolls down: no rows/cols are set by GetLBEventInfo }
kLBSortOccurred = -10;
kLBSelectionMultChangeClick = -11;
kLBEnterKeyPressed = -12;

{ from the SDK, I never saw them in the reality: }
kLBDataChangeRecursiveClick = -13;
kLBDoubleAllClick = -14;
kLBDoubleRecursiveClick = -15;

{ LB's direct edit, introduced by VW 2020, not accessibile yet (VW 2021) with VS }
kLBQueryInteractionType = -16;
kLBQueryItemValue = -17;
kLBQueryItemListRetrieval = -18;
kLBItemEditCompletionData = -19; 
```

**Event flags:**
- no event: row selection for on-click-toggle control types but no Data Items List is available
- -1 if the user clicks on white space within the List Browser. Can happen if your List Browser is higher than the rows displayed. After the last row some white space displays and clicks on this space cause event "-1".
- event = -2: row selection for on-click-toggle control types when items are available
- event = -4: row selection for control types Static and Number
- event = -8: the user scrolls the LB using the arrow keys. This event sets no vars for the rows or cols: rowIndex is always -1, columIndex is always -1. The involved row will highlight nevertheless. But you have no way to find out what is selected until the user actually clicks on a row.
- event = -9: the user types a string while the focus is on the LB. This behaves the same as event -8. From Julian Carr on the V-list.
- event = -10: column selection 

```pascal
GetLBEventInfo( dialogID: LONGINT; componentID: LONGINT; 
	VAR eventType:INTEGER; VAR rowIndex:INTEGER; VAR columIndex:INTEGER):BOOLEAN;
```

[GetLBEventInfo](../../../Function%20Reference/Functions/GetLBEventInfo.md) sets variables with the last event raised, the last selected row and last selected column. Starting with VW 2021, on Windows you can use `GetLBEventInfo` only at the very moment where the user click occurred. Trying to retrieve last user clicks/events after other dialog events will lead to no informations set. This used to be different in previous versions, where you could parse for events any time.

**Important:** you should store as globals last selected row, column, and event.
- If you store selection indexes in global variables, you'll do well to initialize them to -1 and code accordingly. If for some reason `GetLBEventInfo` returns false, you risk misleading values otherwise (for example "0" which would lead to believe a first column or row has selected).
- Setting a sorting column somewhere in your script raises an event. I believe it shouldn't. This will record as last user event. Be careful if you change sorting column after column creation.
- You should always use this routine in an IF condition for the case that it returns FALSE.

**Events on [Drag and Drop](./List%20Browsers%20part%202.md#column-drag-and-drop):** (DG - 2014-03-16)
You need to use the data that comes with the dialog event handler here to catch the drag-drop events!
- event = -4; data = rowIndex: When starting, a normal event is thrown, so just a select event.
- event = -4; data = -50: The first event on releasing the item(s).
- event = -4; data = 43703408: The second event on releasing the item(s).
- event = -4; data = -51: The third and last event on releasing the item(s).
So check for the -51 data to react on drag-drop of items.

**Beastly misleading:** 
- event = 0: you called GetLBEventInfo outside the CASE block AND didn't set a sorting column somewhere in your code 
- eventRow = 0: see above
- eventCol = 0: see above
- event = -10: you called GetLBEventInfo outside the CASE block AND set a sorting column somewhere in your code!
- eventRow = -1: see above
- eventCol = 0: see above

**Probable hint of crashy VW:** 
- event = -<long integer value>: you called GetLBEventInfo outside the CASE block and you got some garbage value from previous codes. I saw this happen but cannot reproduce.
- eventRow = -<long integer value>: see above
- eventCol = -<long integer value>: see above

**Warning:** 
- eventRow = -1: clicking on white space below the last row (for example when your row count doesn't fill the whole available List Browser space).
- eventCol = -1: see above.
- eventCol = 0: default value, before first user's click on the List Browser (for example just after dialog launch). this might be regarded as a bug.
- Resizing columns doesn't return an event parsable with GetLBEventInfo.

**Furthermore:**  it can be observed that image based control types behave differently:
- event = -2: row selection for control types: Static Icon, Multiple Icons
- event = -2: row selection for control types: Radio, Multi State, Single Instance when Column Data Items are defined.
Must have something to do with the Column Data Items wanting to change or these controls expecting them.

**Returns FALSE:** 
- on row selection for control types: Radio, Multi State, Single Instance when Column Data Items are missing (this is a hint that you forgot to set up Column Data Items).

**Unexpectedly returns TRUE:** 
- calling the routine before first user's click on the List Browser (for example just after dialog launch).... and you called it outside the CASE statement for your List Browser ID.

---

## Select

Script-side selection is very well combined with [List Browsers Events](#events), which allows to keep easy track of the last user's selection, if any.

```pascal
SetLBSelection(dialogID: LONGINT; componentID: LONGINT; 
	firstItemIndex: INTEGER; lastItemIndex: INTEGER; select: BOOLEAN): BOOLEAN;
GetNumSelectedLBItems(dialogID: LONGINT; componentID: LONGINT): INTEGER;
IsLBItemSelected(dialogID: LONGINT; componentID: LONGINT; 
	itemIndex: INTEGER): BOOLEAN;
	
EnableLBSingleLineSelection(dialogID: LONGINT; componentID: LONGINT; 
	enable: BOOLEAN): BOOLEAN;
EnableLBClickAllDataChange(dialogID: LONGINT; componentID: LONGINT; 
	enable: BOOLEAN): BOOLEAN;
```

[SetLBSelection](../../../Function%20Reference/Functions/SetLBSelection.md) selects/deselects a range of rows from row `firstItemIndex` to row `lastItemIndex`. If the selection is outside the List Browser's scroll window, the window will automatically scroll to show the selection. See [EnsureLBItemIsVisible](../../../Function%20Reference/Functions/EnsureLBItemIsVisible.md) for a similar behavior, but without selection. This check is not needed if [EnableLBSingleLineSelection](../../../Function%20Reference/Functions/EnableLBSingleLineSelection.md) is active, where the user cannot select more than one line. 

[EnableLBSingleLineSelection](../../../Function%20Reference/Functions/EnableLBSingleLineSelection.md) enables/disables selection of multiple rows. By default multiple selection is enabled. This affects the whole list browser.

[EnableLBClickAllDataChange](../../../Function%20Reference/Functions/EnableLBClickAllDataChange.md) enables/disables changing all cells' values in a column when a modifier key (ctrl/alt on Mac/PC) is pressed. An example of this feature is the Navigation palette: the visibility column. Upon clicking on a row and while multiple rows are selected, the value displayed in the clicked row will apply to all selected rows.

---

## Destroy data

Sometimes what you need is to destroy rows or columns:

```pascal
DeleteLBItem(dialogID: LONGINT; componentID: LONGINT; 
	rowIndex: INTEGER): BOOLEAN; { removes row }
DeleteLBColumn(dialogID: LONGINT; componentID: LONGINT; 
	columnIndex: INTEGER): BOOLEAN; { removes col }
RemoveLBColumnDataItem( dialogID: LONGINT; componentID: LONGINT; 
	columnIndex:INTEGER; columnDataItemIndex:INTEGER):BOOLEAN; { removes col data item }
	
DeleteAllLBItems(dialogID: LONGINT; componentID: LONGINT): BOOLEAN;
RemoveAllLBColumnDataItems( dialogID: LONGINT; componentID: LONGINT; 
	columnIndex:INTEGER);
```

[DeleteLBItem](../../../Function%20Reference/Functions/DeleteLBItem.md) removes the row at `rowIndex` from the List Browser.

[DeleteLBColumn](../../../Function%20Reference/Functions/DeleteLBColumn.md) removes the column at `columnIndex` from the List Browser. If you need to re-write the column headers, you must delete all columns.

[RemoveLBColumnDataItem](../../../Function%20Reference/Functions/RemoveLBColumnDataItem.md) removes the chosen item at `columnDataItemIndex` from the [Column Data Items List](./List%20Browsers%20part%202.md#column-data-items-list) defined for the column at `columnIndex`.

[DeleteAllLBItems](../../../Function%20Reference/Functions/DeleteAllLBItems.md), [RemoveAllLBColumnDataItems](../../../Function%20Reference/Functions/RemoveAllLBColumnDataItems.md).

---

## Update and Refresh

Disable the List Browser updates with [EnableLBUpdates](../../../Function%20Reference/Functions/EnableLBUpdates.md) before looping through a list browser for any operation, reactivate it after the loop has finished executing. If you don't, VW will recalculate the List Browser at each row, each cell inserted. 

Don't forget to re-enable updates and refresh the List Browser using [RefreshLB](../../../Function%20Reference/Functions/RefreshLB.md).
This call should always be the last thing you do after renewing data.

```pascal
EnableLBUpdates(liDialogID, liComponentID : LONGINT; 
	bEnableUpdates :BOOLEAN);
RefreshLB( dialogID: LONGINT; componentID: LONGINT):BOOLEAN;
```

[EnableLBUpdates](../../../Function%20Reference/Functions/EnableLBUpdates.md) enables/disables updating cells in a List Browser. Disable *always* before looping rows with content modification and re-enable after the loop is terminated.

[RefreshLB](../../../Function%20Reference/Functions/RefreshLB.md) redraws the whole List Browser. Keep this outside content modifications involving loops.

---

## Visibility

Useful routines for ensuring that List Browsers are visible:

```pascal
SetFocusOnLB(dialogID: LONGINT; componentID: LONGINT):BOOLEAN;
EnsureLBItemIsVisible( dialogID: LONGINT; componentID: LONGINT; 
	index:INTEGER):BOOLEAN;
```

[SetFocusOnLB](../../../Function%20Reference/Functions/SetFocusOnLB.md) focuses on the chosen List Browser.

[EnsureLBItemIsVisible](../../../Function%20Reference/Functions/EnsureLBItemIsVisible.md) makes the List Browser window display a row even if outside the scroll bounds of the list browser's window. Upon refreshing a List Browser the displayed rows always start at row "0". You don't need this call if you coerce a selection with [SetLBSelection](../../../Function%20Reference/Functions/SetLBSelection.md), the selection will scroll automatically the window to fit.

---

## Enabling

Sometimes you need to make your List Browser not accessible to the user, use [EnableLB](../../../Function%20Reference/Functions/EnableLB.md). The List Browser displays grayed and any user interaction is disabled ([Drag and Drop](./List%20Browsers%20part%202.md#column-drag-and-drop), on-click events). The List Browser is nevertheless fully enabled internally: you can still change content and display by script and it will update as expected.

See [Drag and Drop](./List%20Browsers%20part%202.md#column-drag-and-drop) for disabling dropping only on a range of rows (instead of disabling the whole list browser).

```pascal
EnableLB(dialogID: LONGINT; componentID: LONGINT; 
	enable: BOOLEAN): BOOLEAN;
```

[EnableLB](../../../Function%20Reference/Functions/EnableLB.md) enables/disables a List Browser. Disabled: not clickable and grayed.

---

## User Data

Elsewhere called "itemData". Never figured this out. 
One could think that it expects a resource index, similar to `CreateControl`, but it doesn't. Since it demands a Longint, 

I also tipped on indexed resources (records, symbols, images...) or a list created with BuildResourceList, but this must be a wrong concept. Another possibility is that it expects a handle to some sub-object, but we cannot pass it with Vectorscript. For example user data objects of type 76 accompanying some parametric objects or records of certain kinds (textures, sketches...). Last possibility: too much fantasy and is just unsupported.
Or does it perhaps await data from another dialog?
I have no idea if this should be initialized to "0" or "-1". And I still didn't encounter a situation where this matters. Intuitively I'd say that init on "0" is well.
You will find a reference to this mysterious type of data in the routines below:

- [InsertLBColumnDataItem](../../../Function%20Reference/Functions/InsertLBColumnDataItem.md): targets a column and add something to the particular column data item using the parameter "itemData"? What is that we can add here?
- [GetLBColumnDataItemInfo](../../../Function%20Reference/Functions/GetLBColumnDataItemInfo.md): securely get infos of the mysterious thing added at the particular column data item. Whatever that might be.
- [SetLBItemData](../../../Function%20Reference/Functions/SetLBItemData.md): *broken in VW 2017*, either this or `GetLBItemData` doesn't work any longer, but it did. It targets a cell. Changing it to any possible value didn't ever produce a result by me, but the value set with it could be fetched using GetLBItemData.
- [GetLBItemData](../../../Function%20Reference/Functions/GetLBItemData.md): *broken in VW 2017*, either this or `SetLBItemData` doesn't work any longer, but it did, returning what was set with `SetLBItemData`.

| [Part 1: Creation](./List%20Browsers%20part%201.md) | [Part 2: Columns](./List%20Browsers%20part%202.md) | [Part 3: Rows and Cells](./List%20Browsers%20part%203.md) | [Part 4: Events](./List%20Browsers%20part%204.md) |

---

## Examples

### Example: fetch event, row and column

```pascal
{put in SetupDialogC case }
CASE item OF
SetupDialogC:
	BEGIN
		{ set up the list browser listBrowserID }
		{ ... }
	END;

{ on some event in the list browser, parse event, rowand column }
listBrowserID:
	IF GetLBEventInfo(dlog, listBrowserID, event, eventRow, eventCol) THEN
		alrtDialog(concat('event: ', event, ' last sel row: ', eventRow, ' last sel col: ', eventCol));
END;
{ ... }
```

### Example: select all rows

```pascal
{ _c_ ********************************************* }
{ Selects / Deselects all LB rows }
PROCEDURE LB_SetSelAllRows(d, LB: LONGINT; select: BOOLEAN);
	VAR
		temp_b : BOOLEAN;
	BEGIN
		IF GetNumLBItems(d, LB) > 0 THEN
			temp_b := SetLBSelection(d, LB, 0, GetNumLBItems(d, LB)-1, select);
	END;
```

### Example: deselect all rows

```pascal
{ _c_ ******************************************** }
{ Deselects all rows in a LB }
PROCEDURE LB_DeselectAllLBrows(d, LB: LONGINT);
	VAR
		temp_b : BOOLEAN;
	BEGIN
		temp_b := SetLBSelection(d, LB, 0, GetNumLBItems(d, LB) -1, FALSE);
	END;
```

### Example: deselect selected rows

```pascal
{ _c_ ********************************************* }
{ Delete selected LB items }
PROCEDURE LB_DeleteSelRows(d, LB: LONGINT);
	VAR
		i : INTEGER;
		temp_b : BOOLEAN;
	BEGIN
		i := 0;
		WHILE i < GetNumLBItems(d, LB) DO
			IF IsLBItemSelected(d, LB, i) THEN
				temp_b := DeleteLBItem(d, LB, i)
			ELSE
				i := i + 1;
	END;
```

### Example: delete all columns

```pascal
{ _c_ ******************************************** }
{ Deletes all columns in a LB }
PROCEDURE LB_DeleteAllLBcols(d, LB: LONGINT);
	VAR
		temp_b : BOOLEAN;
	BEGIN
		temp_b := DeleteAllLBItems(d, LB); { remove all rows }
		
		WHILE GetNumLBColumns(d, LB) > 0 DO BEGIN
			RemoveAllLBColumnDataItems(d, LB, 0); { remove all data items }
			temp_b := DeleteLBColumn(d, LB, 0);
		END;
	END;
```
