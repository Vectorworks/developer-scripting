# GetImagePopupObjectItemIndex

## Description
Return item index for the specified object (or zero if not found).

```pascal
FUNCTION GetImagePopupObjectItemIndex(
				dialogID    : LONGINT;
				componentID : LONGINT;
				objectName  : STRING): INTEGER;
```

```python
def vs.GetImagePopupObjectItemIndex(dialogID: int, componentID: int, objectName: str):
    return int
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|
|objectName|STRING|Name of object for which the image popup index should be retrieved.|

## Examples
==== VectorScript ====
```pascal
imagePopupIndex := GetImagePopupObjectItemIndex(dialogID, componentID, 'Symbol-1');
```
==== Python ====
```python
imagePopupIndex = vs.GetImagePopupObjectItemIndex(dialogID, componentID, 'Symbol-1')
vs.SetImagePopupSelectedItem(dialogID, componentID, imagePopupIndex)
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
