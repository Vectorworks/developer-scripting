# CreatePushButton

## Description
Creates a new push button control in a dialog layout.

```pascal
PROCEDURE CreatePushButton(
				dialogID : LONGINT;
				itemID   : LONGINT;
				text     : STRING);
```

```python
def vs.CreatePushButton(dialogID, itemID, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|text|STRING|The display text for the control.|

## Remarks
[DWD 1/20/00]

## Examples
```pascal
BEGIN
	CreateGroupBox (dialogID, 5, '', FALSE);
	CreatePushButton (dialogID, 3, GetPlugInString (3021));
	CreatePushButton (dialogID, 4, GetPlugInString (3022));
END;

CreateStaticText(dialogID, 17, GetPlugInString(4017){'Select a field to specify:'}, -1);
CreateListBox(dialogID, 18, 33, 8);
CreateStaticText(dialogID, 19, GetPlugInString(4019){'Selected field value:'}, -1);
CreateEditText(dialogID, 20, GetPlugInString(4020){'Field Value'}, 13);
CreatePushButton(dialogID, 21, GetPlugInString(4021){'Set'});
CreatePushButton(dialogID, 23, GetPlugInString(4023){'Options...'});
CreateStaticText(dialogID, 24, GetPlugInString(4024){'ID Type:'}, -1);

CreateStaticText         (dialog1, 55,  GetStr(55), -1);
CreateEditText           (dialog1, 56,  GetStr(56), 30);
CreateStaticText         (dialog1, 57,  GetStr(57), -1);
CreateEditText           (dialog1, 58,  GetStr(58), 30);
CreatePushButton         (dialog1, 59,  GetStr(59));
CreatePushButton         (dialog1, 60,  GetStr(60));
CreateCheckBox           (dialog1, 62,  GetStr(62));
```
```python
import vs

# Creates a new push button control in a dialog layout.
dialogID = 1
itemID = 2
text = 'Example text'

vs.CreatePushButton(dialogID, itemID, text)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
