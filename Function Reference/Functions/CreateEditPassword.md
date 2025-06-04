# CreateEditPassword

## Description
Creates an password text field control in a dialog layout.

```pascal
PROCEDURE CreateEditPassword(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				widthInStdChar : LONGINT);
```

```python
def vs.CreateEditPassword(dialogID, itemID, widthInStdChar):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInStdChar|LONGINT|The width of the displayed text in standard character count. See GetDlgCtrlWidthStdCh.|

## Examples
```python
PROCEDURE Example;
VAR
	dialog1 :INTEGER;
	result  :INTEGER;
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;
BEGIN
	dialog1 := CreateLayout('Example Dialog', FALSE, 'OK', 'Cancel');
	CreateEditPassword(dialog1, 4, 16);
	SetFirstLayoutItem(dialog1, 4);
	result := RunLayoutDialog(dialog1, Dialog_Handler);
END;
RUN(Example);
```

## See Also
VS Functions:
[GetDlgCtrlWidthStdCh](GetDlgCtrlWidthStdCh.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
