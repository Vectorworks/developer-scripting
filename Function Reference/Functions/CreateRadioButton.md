# CreateRadioButton

## Description
Creates a new radio button control in a dialog layout.

Radio button groups can be created by defining two or more radio buttons with consecutive index values. When defined as a button group, VectorScript will handle selection-deselection of controls within the group.

```pascal
PROCEDURE CreateRadioButton(
				dialogID : LONGINT;
				itemID   : LONGINT;
				text     : STRING);
```

```python
def vs.CreateRadioButton(dialogID, itemID, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|text|STRING|The display text for the control.|

## Remarks

## Examples
[ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
{* Create dialog control items *}
	{* Method *}
	CreateGroupBox (dialogID, 3, GetPlugInString (3004), TRUE);
	CreateRadioButton (dialogID, 4, GetPlugInString (3005));
	CreateRadioButton (dialogID, 5, GetPlugInString (3006));
	CreateEditText (dialogID, 6, '', 20);
	CreateEditText (dialogID, 7, '', 20);

{* If attribute not used *}
CreateGroupBox (dialogID, 20, GetPlugInString (3016), TRUE);
CreateRadioButton (dialogID, 21, GetPlugInString (3017));
CreateRadioButton (dialogID, 22, GetPlugInString (3018));

BEGIN
	dialog1 := CreateLayout(GetStr(3), TRUE, GetStr(1), GetStr(2));
	CreateGroupBox    (dialog1, kMainGroup,         GetStr(kMainGroup), TRUE);
	CreateRadioButton (dialog1, kReconcileAll,      GetStr(kReconcileAll));
	CreateRadioButton (dialog1, kReconcileSelected, GetStr(kReconcileSelected));
	CreateRadioButton (dialog1, kReconcileThese,    GetStr(kReconcileThese));
	CreateCheckBox    (dialog1, kLegacyTextNotes,   GetStr(kLegacyTextNotes));
	CreateCheckBox    (dialog1, kLegacyKeyNotes,    GetStr(kLegacyKeyNotes));
```
```python
import vs

# Creates a new radio button control in a dialog layout.
dialogID = 1
itemID = 2
text = 'Example text'

vs.CreateRadioButton(dialogID, itemID, text)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
