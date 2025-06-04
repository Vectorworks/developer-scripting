# CreateEditText

## Description
Creates an editable text field control in a dialog layout.

```pascal
PROCEDURE CreateEditText(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				defaultText       : STRING;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateEditText(dialogID, itemID, defaultText, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|defaultText|STRING|The default display text for the control.|
|widthInCharacters|LONGINT|The width of the displayed text in characters.|

## Remarks
In the handler for the new Layout manager, tabbing into and out of an edit field does not produce an event as it did in the classic dialog handler.

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
CreateEditText(dialog1, 4, 'default text', 16);
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
	vs.CreateEditText(dialog1, 4, 'default text', 16)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
