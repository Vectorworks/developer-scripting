# CreateListBox

## Description
Creates a new list box control in a dialog layout.

```pascal
PROCEDURE CreateListBox(
				dialogID           : LONGINT;
				itemID             : LONGINT;
				widthInCharacters  : LONGINT;
				heightInCharacters : LONGINT);
```

```python
def vs.CreateListBox(dialogID, itemID, widthInCharacters, heightInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInCharacters|LONGINT|The width of the control in characters.|
|heightInCharacters|LONGINT|The height of the control in characters.|

## Remarks
This control does not support multiple selections.

## Examples
[DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)

```pascal
CreateEditText(dialogID, 14, GetPlugInString(4014){'Pfx'}, 7);
CreateEditText(dialogID, 15, GetPlugInString(4015){'Lbl'}, 7);
CreateEditText(dialogID, 16, GetPlugInString(4016){'Sfx'}, 7);
CreateStaticText(dialogID, 17, GetPlugInString(4017){'Select a field to specify:'}, -1);
CreateListBox(dialogID, 18, 33, 8);
CreateStaticText(dialogID, 19, GetPlugInString(4019){'Selected field value:'}, -1);
CreateEditText(dialogID, 20, GetPlugInString(4020){'Field Value'}, 13);
CreatePushButton(dialogID, 21, GetPlugInString(4021){'Set'});
CreatePushButton(dialogID, 23, GetPlugInString(4023){'Options...'});

CreateListBox(dialogID, 6, 51, 8);

{Create Dialog control items}
	IF IsMac THEN CreateStaticText(dialogID, 4, GetPlugInString(3006), -1)
	ELSE CreateStaticText(dialogID, 4, GetPlugInString(3005), -1);
	CreateListBox(dialogID, 6, 51, 8);
```
```python
import vs

# Creates a new list box control in a dialog layout.
dialogID = 1
itemID = 2
widthInCharacters = 3
heightInCharacters = 10

vs.CreateListBox(dialogID, itemID, widthInCharacters, heightInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
