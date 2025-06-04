# CreateSearchEditBox

## Description
Creates a search field control in a dialog layout.

```pascal
PROCEDURE CreateSearchEditBox(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				promptText     : STRING;
				widthInStdChar : LONGINT);
```

```python
def vs.CreateSearchEditBox(dialogID, itemID, promptText, widthInStdChar):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|promptText|STRING|The default prompt text for the search control.|
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
	CreateSearchEditBox(dialog1, 4, 'search', 16);
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
