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
CreateEditText(dialog1, 4, 'default text', 16);
SetFirstLayoutItem(dialog1, 4);
result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```
#### Python ####
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

```pascal
{* Create dialog control items *}
{* Arc Length *}
CreateStaticText (dialogID, 3, fieldS [4], -1);
CreateEditText (dialogID, 4, '', 20);

{* Method *}
CreateGroupBox (dialogID, 3, GetPlugInString (3004), TRUE);
CreateRadioButton (dialogID, 4, GetPlugInString (3005));
CreateRadioButton (dialogID, 5, GetPlugInString (3006));
CreateEditText (dialogID, 6, '', 20);
CreateEditText (dialogID, 7, '', 20);

	CreateCheckBox (dialogID, 2*i+5, '');
	CreateStaticText (dialogID, 600+2*i, fieldName [fieldNum], labelWidth);
	CreateSwapControl (dialogID, 2*i+6);
	CreateGroupBox    (dialogID, 300+2*i, '', TRUE);
	CreateEditText    (dialogID, 301+2*i, '', 45);
	CreateGroupBox    (dialogID, 400+2*i, '', TRUE);
	CreatePullDownMenu(dialogID, 401+2*i, 45);
END;
```
```python
import vs

# Creates an editable text field control in a dialog layout.
dialogID = 1
itemID = 2
defaultText = 'Example text'
widthInCharacters = 3

vs.CreateEditText(dialogID, itemID, defaultText, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
