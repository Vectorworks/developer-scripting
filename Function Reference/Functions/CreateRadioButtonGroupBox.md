# CreateRadioButtonGroupBox

## Description
Creates a radio button group box.  The radio button will have name as its label.  If hasFrame is true, the group will have a box drawn around it like a regular group box.

```pascal
PROCEDURE CreateRadioButtonGroupBox(
				dialogID : LONGINT;
				itemID   : LONGINT;
				name     : STRING;
				hasFrame : BOOLEAN);
```

```python
def vs.CreateRadioButtonGroupBox(dialogID, itemID, name, hasFrame):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the radio button group box|
|name|STRING|Title that appears in the radio button group box|
|hasFrame|BOOLEAN|True whether the group has a frame; false otherwise|

## Examples
```pascal
dialog2 := CreateLayout(GetStr( 3), TRUE, GetStr(kOK), GetStr(kCancel));
CreateRadioButtonGroupBox(dialog2, kLineGroup,         GetStr(kLineGroup), TRUE);
CreateStaticText         (dialog2, kBearingLab,        bearingLab, GetDlgCtrlWidthStdCh(bearingLab));
CreateEditText           (dialog2, kBearing,           '', boxWidth);
CreateStaticText         (dialog2, kDistanceLab,       GetStr(kDistanceLab), -1);
CreateEditReal           (dialog2, kDistanse,          kEditRealDim, 0.0, boxWidth);

BEGIN
	dialogID_Out := CreateLayout(GetPlugInString(9003),TRUE,GetPlugInString(9001),'');
	CreateRadioButtonGroupBox(dialogID_Out, 6, GetPlugInString(9006), TRUE);
	CreateStaticText  (dialogID_Out, 7, GetPlugInString(9007),-1);
	CreateEditReal    (dialogID_Out, 8, 3, 0, 8);
	CreateStaticText  (dialogID_Out, 9, GetPlugInString(9009),-1);
	CreatePullDownMenu(dialogID_Out,10, 14);

BEGIN
	dialogID := CreateLayout(GetPlugInString(3003), TRUE, GetPlugInString(3001), GetPlugInString(3002));
	CreateRadioButtonGroupBox(dialogID, kTextGroup,         GetPlugInString(3006), TRUE);
	CreateStaticText         (dialogID, kLabelIndentLab,    GetPlugInString(3007), -1);
	CreateEditReal           (dialogID, kLabelIndent,       3, 0, 7);
	CreateStaticText         (dialogID, kNoteIndentLab,     GetPlugInString(3009), -1);
	CreateEditReal           (dialogID, kNoteIndent,        3, 0, 7);
```
```python
import vs

# Creates a radio button group box.
dialogID = 1
itemID = 2
name = 'Example'
hasFrame = True

vs.CreateRadioButtonGroupBox(dialogID, itemID, name, hasFrame)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
