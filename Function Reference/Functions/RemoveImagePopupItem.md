# RemoveImagePopupItem

## Description
Removes the specified item from the image popup.
The item index lower boundary is 1 not 0. The upper boundary is the number of items in the image popup.

```pascal
PROCEDURE RemoveImagePopupItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER);
```

```python
def vs.RemoveImagePopupItem(dialogID, componentID, itemIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|
|itemIndex|INTEGER|Index to item to be removed.|

## Examples
#### VectorScript ####
```pascal
RemoveImagePopupItem(dialogID, componentID, 4);
```
Variant implementation of RemoveAllImagePopupItems VS function:
```pascal
PROCEDURE ManuallyRemoveAllImagePopupItems(dialogID, componentID :LONGINT);
VAR
	choicesCount, itemIndex: INTEGER;
BEGIN
	choicesCount 	:= GetNumImagePopupItems(dialogID, componentID);
	itemIndex 	:= 1;
	WHILE itemIndex <= choicesCount DO BEGIN
		RemoveImagePopupItem(dialogID, componentID, itemIndex);
		itemIndex := itemIndex + 1;
	END;
END;
```
#### Python ####
```python

```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
