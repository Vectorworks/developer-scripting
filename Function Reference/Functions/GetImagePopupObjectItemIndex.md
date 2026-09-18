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
#### VectorScript ####
```pascal
imagePopupIndex := GetImagePopupObjectItemIndex(dialogID, componentID, 'Symbol-1');
```
#### Python ####
```python
imagePopupIndex = vs.GetImagePopupObjectItemIndex(dialogID, componentID, 'Symbol-1')
vs.SetImagePopupSelectedItem(dialogID, componentID, imagePopupIndex)
```

```pascal
	{ Get the name of the selected item.  It may not be the same as when the user
	  clicked it because of Default Content or an import rename, so get it
	  directly from the HANDLE. }
	SymName := GetName( selectedItemHandle );
	index := GetImagePopupObjectItemIndex( dialogID, PopupID, SymName);
	SetImagePopupSelectedItem( dialogID, PopupID, index );
END;

				LoadTextPopup(symDefs[cnt].symName);
				END;
			END;
		END;
	SetImagePopupSelectedItem(selectSymbol, kSyms, GetImagePopupObjectItemIndex(selectSymbol, kSyms, tmpSymName));
END;

	SetControlText(dialog1, 8, num2strf(str2num(getrfield(unique_plants[temp_i+1],'Plant','spread'))));
	END;
END;
5:	BEGIN {Image Popup}
temp_i := GetImagePopupObjectItemIndex(dialog1,5,GetCurrImgName(dialog1,5));
SelectChoice(dialog1, 4,temp_i - 1,TRUE);
SetControlText(dialog1, 8, num2strf(str2num(getrfield(unique_plants[temp_i],'Plant','spread'))));
	END;
```
```python
import vs

# Return item index for the specified object (or zero if not found).
dialogID: int = 1
componentID: int = 2
objectName: str = 'Example'

result = vs.GetImagePopupObjectItemIndex(dialogID: int, componentID: int, objectName: str)
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
