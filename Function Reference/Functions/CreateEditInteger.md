# CreateEditInteger

## Description
Creates an editable text field control for INTEGER and LONGINT values.

CreateEditInteger is intended specifically for entry of numeric values; the control returns values in a numeric format, and supports calculations within the control field.

```pascal
PROCEDURE CreateEditInteger(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				defaultValue      : LONGINT;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateEditInteger(dialogID, itemID, defaultValue, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|defaultValue|LONGINT|Default value for the field.|
|widthInCharacters|LONGINT|Width of the field in characters.|

## Remarks
Edits long ints, does math,  get and set values with get and set integer calls

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
CreateEditInteger(dialog1, 4, 123, 16);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
```python
def Dialog_Handler( item , data):
	pass

def Example():
	dialog1 = vs.CreateLayout('Example Dialog', False, 'OK', 'Cancel')
	vs.CreateEditInteger(dialog1, 4, 123, 16)
	vs.SetFirstLayoutItem(dialog1, 4)
	result = vs.RunLayoutDialog(dialog1, Dialog_Handler)
Example()
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
