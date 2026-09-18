# CreateCheckBox

## Description
Creates a check box control in a dialog layout.

```pascal
PROCEDURE CreateCheckBox(
				dialogID : LONGINT;
				itemID   : LONGINT;
				text     : STRING);
```

```python
def vs.CreateCheckBox(dialogID, itemID, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|text|STRING|The display text for the control.|

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
CreateCheckBox(dialog1, 4, 'Use layer colors');
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler(item, data):
	pass	
def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateCheckBox(dialog1, 4, 'Use layer colors')
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

```pascal
{* Use Mouse Clicks... *}
CreateCheckBox (dialogID, 7, fieldS [6]);
CreateStaticText (dialogID, 8, fieldS [7], -1);

BEGIN
	fieldNum := n1 + i - 1;
	CreateCheckBox (dialogID, 2*i+5, '');
	CreateStaticText (dialogID, 600+2*i, fieldName [fieldNum], labelWidth);
	CreateSwapControl (dialogID, 2*i+6);
	CreateGroupBox    (dialogID, 300+2*i, '', TRUE);
	CreateEditText    (dialogID, 301+2*i, '', 45);

{* Attributes to use *}
CreateGroupBox (dialogID, 10, GetPlugInString (3007), TRUE);
CreateGroupBox (dialogID, 30, '', FALSE);
CreateGroupBox (dialogID, 35, '', FALSE);
CreateCheckBox (dialogID, 11, GetPlugInString (3008));
CreateCheckBox (dialogID, 12, GetPlugInString (3009));
CreateCheckBox (dialogID, 13, GetPlugInString (3010));
CreateCheckBox (dialogID, 14, GetPlugInString (3011));
CreateGroupBox (dialogID, 31, '', FALSE);
```
```python
import vs

# Creates a check box control in a dialog layout.
dialogID = 1
itemID = 2
text = 'Example text'

vs.CreateCheckBox(dialogID, itemID, text)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
SetItem
| SetItemEnable
| ItemSel

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
