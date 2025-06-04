# GetImagePopupObject

## Description
Returns the object name for the specified image popup item.

```pascal
FUNCTION GetImagePopupObject(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER): STRING;
```

```python
def vs.GetImagePopupObject(dialogID, componentID, itemIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|
|itemIndex|INTEGER|Image popup item index for object to be retrieved.|

## Remarks
This procedure returns the name of the resource found in an image pop-up control at a specified index location in that pop-up.

-Component ID is the index to the dialog Item number for the control<BR>
-ItemIndex is the index to the item you wish to find the resource name<BR>
-ObjectName returns the resource name of the resource that is found in the image pop-up control at index itemIndex.<BR>
-This function will only return the name for resources in the current document.  It will return an empty string if the resource is not in the document.

## Examples
#### VectorScript ####
```pascal
objectName := GetImagePopupObject(dialogID, componentID, 4);
```
#### Python ####
```python
objectName = vs.GetImagePopupObject(dialogID, componentID, 4)
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [SetImagePopupSelectedItem](SetImagePopupSelectedItem.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
