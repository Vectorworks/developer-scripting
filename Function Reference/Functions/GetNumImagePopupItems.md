# GetNumImagePopupItems

## Description
Returns the number of items in the image popup.

```pascal
FUNCTION GetNumImagePopupItems(
				dialogID    : LONGINT;
				componentID : LONGINT): INTEGER;
```

```python
def vs.GetNumImagePopupItems(dialogID, componentID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|

## Examples
==== VectorScript ====
```pascal
numImagePopupItems := GetNumImagePopupItems(dialogID, componentID);
```
==== Python ====
```python
numImagePopupItems = vs.GetNumImagePopupItems(dialogID, componentID)
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
