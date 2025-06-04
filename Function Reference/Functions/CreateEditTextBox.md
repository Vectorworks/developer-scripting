# CreateEditTextBox

## Description
Creates a scrolling multiline editable text field in a dialog layout.

```pascal
PROCEDURE CreateEditTextBox(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				defaultText       : STRING;
				widthInCharacters : LONGINT;
				heightInLines     : LONGINT);
```

```python
def vs.CreateEditTextBox(dialogID, itemID, defaultText, widthInCharacters, heightInLines):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog|
|itemID|LONGINT|The id of the text box control.|
|defaultText|STRING|The initial text.|
|widthInCharacters|LONGINT|Width of the control in characters|
|heightInLines|LONGINT|Height of the control in lines.|

## Examples
==== VectorScript ====
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
CreateEditTextBox(dialog1, 4, 'default text', 24, 16);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
==== Python ====
```python
def Dialog_Handler( item , data ):
	pass
def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateEditTextBox(dialog1, 4, 'default text', 24, 16)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
