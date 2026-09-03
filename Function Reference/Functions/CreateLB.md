# CreateLB

## Description
Creates a layout manager list browser control.

```pascal
PROCEDURE CreateLB(
				dialogID           : LONGINT;
				componentID        : LONGINT;
				widthInCharacters  : INTEGER;
				heightInCharacters : INTEGER);
```

```python
def vs.CreateLB(dialogID, componentID, widthInCharacters, heightInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|widthInCharacters|INTEGER|the width of the control in characters|
|heightInCharacters|INTEGER|the height of the control in characters|

## Remarks
(*\_c\_*, 2022.01.22) : Here the former Vectorlab article: [[User:CBM-c-/VS-List_Browsers_part_1| List Browsers]]

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
CreateCheckBox( dlgId, kSetSlabCheck, GetPluginString(3022) );
CreateStaticText( dlgId, kSlabThicknessLabel, GetPluginString(3023), -1 );
CreateEditReal( dlgId, kSlabThicknessEdit, 1, 0.0, 20 );
CreateGroupBox( dlgId, kLBSettingsPanel, '', False );
CreateLB( dlgId, kLBCtrl, 70, 10 );
CreateGroupBox( dlgId, kSelectedFloor, GetPluginString(3024), True );
CreateStaticText( dlgId, kClassLabel, GetPluginString(3025), _grpWidth_1 );
CreateClassPullDownMenu( dlgId, kClassPopup, 27 );
CreateStaticText( dlgId, kElevationLabel, GetPluginString(3026), _grpWidth_1 );

BEGIN
	dialogID := CreateResizableLayout(GetPluginString(3006), TRUE, GetPluginString(3004), GetPluginString(3005), TRUE, TRUE);
	CreateLB(dialogID, kHeliodonList, 80, 20);
	SetFirstLayoutItem(dialogID, kHeliodonList);
	SetHelpText(dialogID, kOK, GetPluginString(3009));
	SetHelpText(dialogID, kCancel, GetPluginString(3010));
	SetHelpText(dialogID, kHeliodonList, GetPluginString(3007));

BEGIN
	dialogID := CreateResizableLayout (GetPluginString(3003), TRUE, GetPluginString(3001), GetPluginString(3002), TRUE, TRUE);
	{dialogID := CreateLayout(GetPluginString(3003),TRUE,GetPluginString(3001),GetPluginString(3002));}
	CreateStaticText(dialogID,4,GetPluginString(3004),-1);
	CreateLB(dialogID,5,60,8);
	CreateStaticText(dialogID,6,GetPluginString(3006),-1);
	CreatePulldownMenu(dialogID,7,16);
	CreatePushButton(dialogID,8,GetpluginString(3008));
```
```python
import vs

# Creates a layout manager list browser control.
dialogID = 1
componentID = 2
widthInCharacters = 3
heightInCharacters = 10

vs.CreateLB(dialogID, componentID, widthInCharacters, heightInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
