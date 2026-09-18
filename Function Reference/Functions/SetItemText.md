# SetItemText

## Description
Sets the text for the specified text component.

```pascal
PROCEDURE SetItemText(
				dialogID    : LONGINT;
				componentID : LONGINT;
				text        : DYNARRAY[] of CHAR);
```

```python
def vs.SetItemText(dialogID, componentID, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the text component.|
|text|DYNARRAY[] of CHAR|The text that should be placed in the text component.|

## Examples
```pascal
BEGIN
	CASE item OF
		{* dialog init *}
		SetupDialogC: BEGIN
			SetItemText(dialogID, 4, Num2StrF (0));
			SetItemText(dialogID, 6, Num2StrF (0));
			SetBooleanItem(dialogID, 7, FALSE);
			SelectEditText(dialogID, 4);
		END;

SetItemText(dialogID, 6, Num2Str (0, nSegs));
EnableItem(dialogID, 6, (method = 1));

	DisplaySwapPane (gCurrentDialogID, swapControlID, 2);
	EnableItem(gCurrentDialogID, pulldownID, gChangeField [fieldNum]);
END
ELSE BEGIN
	SetItemText(gCurrentDialogID, editTextID, gNewValue [fieldNum]);
	DisplaySwapPane (gCurrentDialogID, swapControlID, 1);
	EnableItem(gCurrentDialogID, editTextID, gChangeField [fieldNum]);
END;
```
```python
import vs

# Sets the text for the specified text component.
dialogID = 1
componentID = 2
text = 'Example text'

vs.SetItemText(dialogID, componentID, text)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
