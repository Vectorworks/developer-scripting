# GetImagePopupSelectedItem

## Description
Gets the selected image popup item.

```pascal
FUNCTION GetImagePopupSelectedItem(
				dialogID    : LONGINT;
				componentID : LONGINT): INTEGER;
```

```python
def vs.GetImagePopupSelectedItem(dialogID, componentID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|

## Remarks
Returns the index to the Item that is currently selected in the image pop-up control.  Currently there is always a selected item.

ComponentID is the dialog Item index of the control

This function is currently returning item indexes assuming a 1-based index whereas GetImagePopupObject() assumes a zero based index.  This will hopefully be fixed for release so that all layout mgr dialog controls use a zero based indexing system for lists of items.

## Examples
#### VectorScript ####
```pascal
selectedItemIndex := GetImagePopupSelectedItem(dialogID, componentID);
```
#### Python ####
```python
selectedItemIndex = vs.GetImagePopupSelectedItem(dialogID, componentID)
```

```pascal
		ELSE CreateSeatSym(symName);
END
ELSE IF shouldUseExisting THEN BEGIN
	IF selSymFolder = GetPluginString(4012) THEN BEGIN { symbol is in a defaults document }
		choiceNum := GetImagePopupSelectedItem(selectSymbol, kSyms);
		IF choiceNum <= defaultListCount THEN
			symHandle := ImportResourceToCurrentFile(defaultListID, choiceNum)
		ELSE
			symHandle := ImportResourceToCurrentFile(defaultListID2, choiceNum-defaultListCount);

tempInt := GetImagePopupSelectedItem( dialog1, kImagePopup5 );
tempShapeName := gSymbolInfo [tempInt].shapeName;
gSymbolName := gSymbolInfo[tempInt].symbolName;

BEGIN
	Symbolidx := GetImagePopupSelectedItem(SelectRepSymbol, kImagePopup6);
	h := ResList_ImportItem( kRepetUnitSymbols );
	if h <> NIL THEN
	BEGIN
		SymbolName := GetName(h);
```
```python
import vs

# Gets the selected image popup item.
dialogID = 1
componentID = 2

resultN = vs.GetImagePopupSelectedItem(dialogID, componentID)
vs.Message('GetImagePopupSelectedItem returned: ' + str(resultN))
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
