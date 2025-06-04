# InsertImagePopupObjectItem

## Description
Inserts the specified object into the image popup.

Note: the image popup only supports the following object types: gradients, hatches, images, record formats, render backgrounds, symbol folders, symbols, textures, vectorscript palettes, vectorscripts, worksheets.

```pascal
FUNCTION InsertImagePopupObjectItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				objectName  : STRING): INTEGER;
```

```python
def vs.InsertImagePopupObjectItem(dialogID, componentID, objectName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|
|objectName|STRING|Name of the object to insert.|

## Remarks
Functionality description needs more.

Inserts the specified object into the image popup.

The object specified by ObjectName must be the name of a previewable object.  Passing it the name of an object in the document does not work.  Symbol Definitions, Gradients, Hatches, Image Resources, Textures, and RedSymbols(?) are valid things to pass to this function.  The return value is the index to the item in the pop-up.  This index value can change as items are added and removed from the list and should not be counted on to be a good reference to a particular resource.

Items are inserted and maintained in alphabetic order this may cause items to be inserted into the existing list, changing the indices of previous items.

If an Item fails to be inserted in the popup the function returns zero as the pop-up index value.

## Examples
#### VectorScript ####
```pascal
PROCEDURE dialog1_Main;
VAR
dialog1 :INTEGER;
int     :INTEGER;
str     :STRING;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
str := GetSDName(FSymDef);
int := InsertImagePopupObjectItem(dialog1, 4, str);
SetImagePopupSelectedItem(dialog1, 4, int);
END;
END;
END;

BEGIN
dialog1 := CreateLayout('Image Pop-Up', FALSE, 'OK', '');
CreateControl(dialog1, 4, 10, '', 0);
SetFirstLayoutItem(dialog1, 4);
int := RunLayoutDialog(dialog1, dialog1_Handler);
END;
RUN(dialog1_Main);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetNumImagePopupItems](GetNumImagePopupItems.md) 
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
