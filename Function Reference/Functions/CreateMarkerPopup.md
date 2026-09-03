# CreateMarkerPopup

## Description
Creates a popup control that displays the various marker styles available in VectorWorks and allows the user to choose one.  Markers are the adornments at the endpoints of line objects and consist of styles like arrow, circle, cross, etc.

```pascal
PROCEDURE CreateMarkerPopup(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.CreateMarkerPopup(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Id of the dialog|
|componentID|LONGINT|Id of the popup control|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
dialog1	:INTEGER;
result	:INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;

BEGIN
dialog1 := CreateLayout('Untitled Dialog', FALSE, 'OK', 'Cancel');
CreateMarkerPopup(dialog1, 4);
SetFirstLayoutItem(dialog1,  4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler( item , data ):
	pass

def Example():
	dialog1 = vs.CreateLayout('Untitled Dialog', False, 'OK', 'Cancel')
	vs.CreateMarkerPopup(dialog1, 4)
	vs.SetFirstLayoutItem(dialog1,  4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)

Example()
```

```pascal
	END
ELSE
CreateCheckBox			(IDLabelDialog, kIDAutoInc, GetPlugInString(6005));		{'Auto-Increment ID Label'}
CreateCheckBox           (IDLabelDialog, kUseMarker,   GetStr(kUseMarkerTxt));
CreateMarkerPopup        (IDLabelDialog, kLeaderStyle);
CreateStaticText		(IDLabelDialog,kBubbleSizeTxt, GetStr(kBubbleSizeTxt),18);
CreateEditReal			(IDLabelDialog,kBubbleSize, 3,0,16);
CreateStaticText		(IDLabelDialog,kBubbleLSTxt, GetStr(kBubbleLSTxt),18);
CreateLineAttributePopup (IDLabelDialog, kBubbleLS);

CreateGroupBox            (dialog1, kPlanDetailGrp,         GetStr(kPlanDetailGrp), TRUE);
CreateCheckBox            (dialog1, kDashedRiserLines,      GetStr(kDashedRiserLines));
CreateCheckBox            (dialog1, kHideRiserLines,        GetStr(kHideRiserLines));
CreateCheckBox            (dialog1, kEndMarkerCB,           GetStr(kEndMarkerCB));
CreateMarkerPopup         (dialog1, kEndMarker);
CreateCheckBox            (dialog1, kBegMarkerCB,           GetStr(kBegMarkerCB));
CreateMarkerPopup         (dialog1, kBegMarker);
CreateStaticText          (dialog1, kArrowClassLab,         GetStr(kArrowClassLab), -1);
CreateClassPullDownMenu   (dialog1, kArrowClass,            generalPopUps);

CreateCheckBox( dialog, kBubbleShadow, GetStr(kBubbleShadow) );
CreateStaticText( dialog, kBubLeadTypePopUpLab, GetStr(kBubLeadTypePopUpLab), -1 );
CreatePulldownMenu( dialog, kBubLeadTypePopUp, 17 );
CreateStaticText( dialog, kBubLeadMarkerLab, GetStr(kBubLeadMarkerLab), -1 );
CreateMarkerPopup( dialog, kBubLeadMarkerPopUp);
```
```python
import vs

# Creates a popup control that displays the various marker styles available
# in VectorWorks and allows the user to choose one.
dialogID = 1
componentID = 2

vs.CreateMarkerPopup(dialogID, componentID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
