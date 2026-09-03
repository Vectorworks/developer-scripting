# RemoveAllImagePopupItems

## Description
Removes all items from the image popup.

```pascal
PROCEDURE RemoveAllImagePopupItems(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.RemoveAllImagePopupItems(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|

## Examples
#### VectorScript ####
```pascal
RemoveAllImagePopupItems(dialogID, componentID);
```
#### Python ####
```python

```

```pascal
BEGIN
	RemoveAllImagePopupItems(selectSymbol, kSyms);
	for cnt := 1 to symDefCnt do BEGIN
		IF symDefs[cnt].folderName = folderName THEN BEGIN
			IF symDefs[cnt].folderLevel >= 0 THEN
				int := InsertImagePopupObjectItem(selectSymbol, kSyms, symDefs[cnt].symName)

{ Populate the Image Popup }
RemoveAllImagePopupItems ( dialogID, PopupID);
FOR index := 1 TO numItems DO
	insertIndex := InsertImagePopupResource( dialogID, PopupID, listID, index );

BEGIN
	RemoveAllImagePopupItems(selectSymbol, kSyms);
	foundTmpSymName := FALSE;
	firstValidSymName := '';
	IF (folderIndex < 1) OR (folderIndex > folderCnt) THEN folderIndex := 1;
	IF folders[folderIndex].isDefaults THEN
```
```python
vs.RemoveAllImagePopupItems(dialogID, componentID)
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
