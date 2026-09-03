# CreateThumbnailPopup

## Description
Creates a thumbnail popup that can be populated with previews of objects in Vectorworks.

```pascal
PROCEDURE CreateThumbnailPopup(
				dialogID  : LONGINT;
				controlID : LONGINT);
```

```python
def vs.CreateThumbnailPopup(dialogID, controlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |

## Remarks
'''BE AWARE:''' this will not work for Line Types of an external document (default library for example). Use [CreateCustThumbPopup](CreateCustThumbPopup.md) in that situation.

## Examples
```pascal
	CreateGroupBox      (dialog1, kGroupBox19Structural,    GetStr(kGroupBox19Structural), TRUE);
	CreateStaticText    (dialog1, kStaticText20Textures,	GetStr(kStaticText20Textures), -1);
	CreatePullDownMenu  (dialog1, kPopup21Textures,			20);
	CreateStaticText 		(dialog1, kStaticTextArchUseMaterial, GetStr(kStaticTextArchUseMaterial), -1);
	CreateThumbnailPopup(dialog1, kPopup23ArchMaterial);
	CreateStaticText 		(dialog1, kStaticTextStructUseMaterial, GetStr(kStaticTextStructUseMaterial), -1);
	CreateThumbnailPopup(dialog1, kPopupStructMaterial);
END;

	CreateStaticText  (selectSymbol, kSymFoldersLab, GetStr(kSymFoldersLab-3), -1);
	CreateListBoxN    (selectSymbol, kSymFolders,    36, 7, FALSE);
	CreateStaticText  (selectSymbol, kSymsLab,       GetStr(kSymsLab-3), -1);
{	CreateControl     (selectSymbol, kSyms,          10, '', 0); }
    CreateThumbnailPopup(selectSymbol, kSyms);
	SetFirstLayoutItem(selectSymbol, kCreateNewRad);
	SetRightItem      (selectSymbol, kCreateNewRad,  kCreateNewName, 0,0);
	SetBelowItem      (selectSymbol, kCreateNewRad,  kUseExisting,   0, 4);
	SetBelowItem      (selectSymbol, kUseExisting,   kHiddenGroup,   4, 0);

CreateThumbnailPopup(dialog, kImagePopup_ProfSyms);
```
```python
import vs

# Creates a thumbnail popup that can be populated with previews of objects in
# Vectorworks.
dialogID = 1
controlID = 2

vs.CreateThumbnailPopup(dialogID, controlID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
