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

## See Also
VS Functions:
[SetItem](SetItem.md) 
| [SetItemEnable](SetItemEnable.md) 
| [ItemSel](ItemSel.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
