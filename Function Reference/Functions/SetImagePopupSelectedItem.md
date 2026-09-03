# SetImagePopupSelectedItem

## Description
Sets the selected image popup item. The itemIndex parameter is 1-based.

```pascal
PROCEDURE SetImagePopupSelectedItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER);
```

```python
def vs.SetImagePopupSelectedItem(dialogID, componentID, itemIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|Index to a specific image popup component.|
|itemIndex|INTEGER|Index to item to select.|

## Examples
#### VectorScript ####
```pascal
SetImagePopupSelectedItem(dialogID, componentID, 4);
```
#### Python ####
```python

```

```pascal
					int := InsertImagePopupResource(selectSymbol, kSyms, defaultListID, symDefs[cnt].resourceIndex);
				END;
		END;
	END;
	SetImagePopupSelectedItem(selectSymbol, kSyms, 1);
END;

END;	{of gNumShapes > 0}
SetImagePopupSelectedItem( dialog1, kImagePopup5, gImagePopup5Int );

	SetImagePopupSelectedItem(SelectMarker, kImagePopup4, Marker1idx);
	SetImagePopupSelectedItem(SelectMarker, kImagePopup5, Marker2idx);
	EnableItem(SelectMarker, kImagePopup5,NOT(Matching));
END;
```
```python
vs.SetImagePopupSelectedItem(dialogID, componentID, 1)
```

## See Also
VS Functions:
[InsertImagePopupObjectItem](InsertImagePopupObjectItem.md) 
| [GetNumImagePopupItems](GetNumImagePopupItems.md) 
| [GetImagePopupObject](GetImagePopupObject.md) 
| [GetImagePopupObjectItemIndex](GetImagePopupObjectItemIndex.md) 
| [GetImagePopupSelectedItem](GetImagePopupSelectedItem.md) 
| [RemoveImagePopupItem](RemoveImagePopupItem.md) 
| [RemoveAllImagePopupItems](RemoveAllImagePopupItems.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
