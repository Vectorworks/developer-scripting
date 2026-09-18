# CreateClassPullDownMenu

## Description
Creates a Layout Manager class pull down menu control.

```pascal
PROCEDURE CreateClassPullDownMenu(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateClassPullDownMenu(nDialogID, nComponentID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInChars|INTEGER|   |

## Remarks
*\_c\_* (2016.02.22): Add the localized string "<Object Class>" below "New...". You must do this during the SetupDialogC event of your dialog driver:
```pascal
GetResourceString(objClassString, 2103, 148); { fetches the localized "<Object Class>" string }
IF InsertPropClassOrLayerItem(dialogID, c_classPullDownMenu_Index, objClassString, '') THEN
	{ do something, eventually };
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
	dialog1 :INTEGER;
	result  :INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
	BEGIN
	END;
BEGIN
	dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
	CreateClassPullDownMenu(dialog1, 4, 24);
	SetFirstLayoutItem(dialog1, 4);
	result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler(item , data ):
	pass
def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateClassPullDownMenu(dialog1, 4, 24)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)

Example()
```

```pascal
BEGIN
	dialog1 := CreateResizableLayout(GetStr( 3), TRUE, GetStr(kOK), GetStr(kCancel), TRUE, TRUE);
	CreateStaticText          (dialog1, kStaticText4Shaft,   		GetStr(kStaticText4Shaft), -1);
	CreateClassPullDownMenu   (dialog1, kPopup5ShaftFinish,        	20);
	CreateStaticText          (dialog1, kStaticText6CapitalFinish,  GetStr(kStaticText6CapitalFinish), -1);
	CreateClassPullDownMenu   (dialog1, kPopup5CapitalFinish,       20);
	CreateStaticText          (dialog1, kStaticText8BaseFinish,   	GetStr(kStaticText8BaseFinish), -1);
	CreateClassPullDownMenu   (dialog1, kPopup5BaseFinish,        	20);

CreateStaticText         (IDLabelDialog, kMarkerStyleTxt,      GetStr(kMarkerStyleTxt), 13);
CreateStaticText         (IDLabelDialog, kLineStyleTxt,      GetStr(kLineStyleTxt), 15);
CreateLineAttributePopup (IDLabelDialog, kIDLeaderLS);
CreateStaticText         (IDLabelDialog, kIDClassTxt,      GetStr(kIDClassTxt), 16);
CreateClassPullDownMenu  (IDLabelDialog, kLabelClass,        16);
CreateGroupBox			 (IDLabelDialog, kGroupBox7,		GetStr(KGroupBox7), FALSE);
CreateCheckBox			 (IDLabelDialog, kAutoRotate,   GetStr(kAutoRotateTxt));
IF EditDoorID | EditWindowID THEN
	BEGIN

CreateGroupBox( dlgId, kLBSettingsPanel, '', False );
CreateLB( dlgId, kLBCtrl, 70, 10 );
CreateGroupBox( dlgId, kSelectedFloor, GetPluginString(3024), True );
CreateStaticText( dlgId, kClassLabel, GetPluginString(3025), _grpWidth_1 );
CreateClassPullDownMenu( dlgId, kClassPopup, 27 );
CreateStaticText( dlgId, kElevationLabel, GetPluginString(3026), _grpWidth_1 );
CreateEditReal( dlgId, kElevationEdit, 1, 0.0, 27 );
CreateStaticText( dlgId, kFloorHeightLabel, GetPluginString(3027), _grpWidth_1 );
CreateEditReal( dlgId, kFloorHeightEdit, 1, 0.0, 27 );
```
```python
import vs

# Creates a Layout Manager class pull down menu control.
nDialogID = 1
nComponentID = 2
nWidthInChars = 3

vs.CreateClassPullDownMenu(nDialogID, nComponentID, nWidthInChars)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[CreateImageControl](CreateImageControl.md), 
[InsertPropClassOrLayerItem](InsertPropClassOrLayerItem.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
