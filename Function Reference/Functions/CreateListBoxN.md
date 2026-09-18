# CreateListBoxN

## Description
Creates a new list box control in a dialog layout. With isMultipleSelect true, the list supports multiple selection.

```pascal
PROCEDURE CreateListBoxN(
				dialogID           : LONGINT;
				itemID             : LONGINT;
				widthInCharacters  : LONGINT;
				heightInCharacters : LONGINT;
				isMultipleSelect   : BOOLEAN);
```

```python
def vs.CreateListBoxN(dialogID, itemID, widthInCharacters, heightInCharacters, isMultipleSelect):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInCharacters|LONGINT|The width of the control in characters.|
|heightInCharacters|LONGINT|The height of the control in characters.|
|isMultipleSelect|BOOLEAN|Does the list support multiple selection|

## Examples
[DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)

```pascal
	CreateEditText    (selectSymbol, kCreateNewName, GetPluginString(4005), 16);
	CreateRadioButton (selectSymbol, kUseExisting,   GetPluginString(4006));
	CreateGroupBox    (selectSymbol, kHiddenGroup,   GetStr(kHiddenGroup), FALSE);
	CreateStaticText  (selectSymbol, kSymFoldersLab, GetStr(kSymFoldersLab-3), -1);
	CreateListBoxN    (selectSymbol, kSymFolders,    36, 7, FALSE);
	CreateStaticText  (selectSymbol, kSymsLab,       GetStr(kSymsLab-3), -1);
{	CreateControl     (selectSymbol, kSyms,          10, '', 0); }
    CreateThumbnailPopup(selectSymbol, kSyms);
	SetFirstLayoutItem(selectSymbol, kCreateNewRad);

CreateListBoxN(dialogID,5,40,21,TRUE);
CreatePushButton(dialogID,6,GetPlugInString(3113));
CreatePushButton(dialogID,7,GetPlugInString(3114));
CreatePushButton(dialogID,8,GetPlugInString(3115));
CreatePushButton(dialogID,9,GetPlugInString(3116));

	selectSymbol := CreateResizableLayout(dialogTitle, TRUE, GetStr(kOK), GetStr(kCancel), TRUE, TRUE);
	CreateGroupBox    (selectSymbol, kTopGroup,      GetStr(kTopGroup), FALSE);
	CreateGroupBox    (selectSymbol, kHiddenGroup,   GetStr(kHiddenGroup), FALSE);
	CreateStaticText  (selectSymbol, kSymFoldersLab, GetStr(kSymFoldersLab), -1);
	CreateListBoxN    (selectSymbol, kSymFolders,    26, 7, FALSE);
	CreateStaticText  (selectSymbol, kSymsLab,       GetStr(kSymsLab), -1);
{	CreateControl     (selectSymbol, kSyms,          10, '', 0); }
    CreateThumbnailPopup(selectSymbol, kSyms);
```
```python
import vs

# Creates a new list box control in a dialog layout.
dialogID = 1
itemID = 2
widthInCharacters = 3
heightInCharacters = 10
isMultipleSelect = True

vs.CreateListBoxN(dialogID, itemID, widthInCharacters, heightInCharacters, isMultipleSelect)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
