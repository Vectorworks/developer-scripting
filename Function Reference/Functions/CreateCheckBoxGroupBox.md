# CreateCheckBoxGroupBox

## Description
Creates a checkbox group box.  The checkbox will have name as its label.  If hasFrame is true, the group will have a box drawn around it like a regular group box.

```pascal
PROCEDURE CreateCheckBoxGroupBox(
				dialogID : LONGINT;
				itemID   : LONGINT;
				name     : STRING;
				hasFrame : BOOLEAN);
```

```python
def vs.CreateCheckBoxGroupBox(dialogID, itemID, name, hasFrame):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the checkbox group box|
|name|STRING|Title that appears in the checkbox group box|
|hasFrame|BOOLEAN|True if the group box has a frame around it; false otherwise|

## Remarks
On VW 12.5.1 Win the border must be set to TRUE. If the border is set to FALSE the application crashes by clicking the checkBoxGroupBox.

On VW 2016 Win the name parameter must have at least 2 characters or the checkbox will not be drawn.

## Examples
[ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
BEGIN
	IDLabelDialog := CreateLayout(GetStr( 3), TRUE, GetStr(kOK), GetStr(kCancel));
	CreateStaticText         (IDLabelDialog, kLabelShapeTxt,       GetStr(kLabelShapeTxt), 16);
	CreatePulldownMenu       (IDLabelDialog, kLabelShape,        16);
	CreateCheckBoxGroupBox   (IDLabelDialog, kShowLeader,        GetStr(kShowLeader), TRUE);
	CreateStaticText         (IDLabelDialog, kMarkerStyleTxt,      GetStr(kMarkerStyleTxt), 13);
	CreateStaticText         (IDLabelDialog, kLineStyleTxt,      GetStr(kLineStyleTxt), 15);
	CreateLineAttributePopup (IDLabelDialog, kIDLeaderLS);
	CreateStaticText         (IDLabelDialog, kIDClassTxt,      GetStr(kIDClassTxt), 16);

CreateEditText           (dialog1, 65,  GetStr(65), 30);
CreateStaticText         (dialog1, 66,  GetStr(66), -1);
CreateEditText           (dialog1, 67,  GetStr(67), 16);
CreateGroupBox           (dialog1, 68,  GetStr(68), FALSE);
CreateCheckBoxGroupBox   (dialog1, 69,  GetStr(69), TRUE);
CreateStaticText         (dialog1, 70,  GetStr(70), -1);
CreateEditText           (dialog1, 71,  GetStr(71), 16);
CreateStaticText         (dialog1, 72,  GetStr(72), -1);
CreateEditText           (dialog1, 73,  GetStr(73), 16);

{issue pane}
CreateCheckBoxGroupBox   (dialogID, 69,  GetPluginString (4069), TRUE);
CreateStaticText         (dialogID, 70,  GetPluginString (4070), -1);
CreateEditText           (dialogID, 71,  GetPluginString (4071), 16);
CreateStaticText         (dialogID, 72,  GetPluginString (4072), -1);
CreateEditText           (dialogID, 73,  GetPluginString (4073), 16);
```
```python
import vs

# Creates a checkbox group box.
dialogID = 1
itemID = 2
name = 'Example'
hasFrame = True

vs.CreateCheckBoxGroupBox(dialogID, itemID, name, hasFrame)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
