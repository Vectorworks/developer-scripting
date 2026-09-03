# ResList_SelFAvail

## Description
Set the first available item in the resource popup. The 'uniqueID' is a string identifier uniquely identifying this control, item name is the item to search for, if not empty, rest is search properties

```pascal
PROCEDURE ResList_SelFAvail(
				uniqueID            : STRING;
				VAR itemName        : STRING;
				onlyCurrentDocument : BOOLEAN;
				searchOnline        : BOOLEAN;
				skipCurrentDocument : BOOLEAN);
```

```python
def vs.ResList_SelFAvail(uniqueID, onlyCurrentDocument, searchOnline, skipCurrentDocument):
    return itemName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|itemName|STRING|   |
|onlyCurrentDocument|BOOLEAN|   |
|searchOnline|BOOLEAN|   |
|skipCurrentDocument|BOOLEAN|   |

## Examples
```pascal
{ResList_SetSel( kMaterialsContent1, localName );}
IF (archCompMaterialNameID = '') THEN
	ResList_SetSelCtrl(kMaterialsContent1, 0)
ELSE BEGIN
	ResList_SelFAvail( kMaterialsContent1, archCompMaterialNameID, FALSE, FALSE, FALSE)
END;

	ResList_SelFAvail( LocID, SelectedSymbol, FALSE, TRUE, FALSE);
END;

	ResList_SelFAvail( kTextureContent, SelectedTexture, FALSE, TRUE, FALSE);
	ResList_DlgInit( kTextureContent, dialog, kImagePickPU );
END;
```
```python
import vs

# Set the first available item in the resource popup.
uniqueID = 'Example'
onlyCurrentDocument = True
searchOnline = True
skipCurrentDocument = True

result = vs.ResList_SelFAvail(uniqueID, onlyCurrentDocument, searchOnline, skipCurrentDocument)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
