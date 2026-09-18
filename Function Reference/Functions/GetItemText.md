# GetItemText

## Description
Gets the text that is contained in the given componentID.

```pascal
PROCEDURE GetItemText(
				dialogID    : LONGINT;
				componentID : LONGINT;
				VAR text    : STRING);
```

```python
def vs.GetItemText(dialogID, componentID):
    return text
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component that the text will be retrieved from.|
|text|STRING|The text of the component.|

## Examples
```pascal
GetItemText(dialogID, 4, tmpStr);

1: BEGIN
	IF method = 1 THEN BEGIN
		GetItemText(dialogID, 6, tmpStr);
		OK := ValidNumStr (tmpStr, nSegs);
		IF (NOT OK) OR (nSegs < 1) THEN
		BEGIN
			Sysbeep;

END
ELSE BEGIN
	editTextID := 301 + 2*i;
	EnableItem(gCurrentDialogID, editTextID, gChangeField [fieldNum]);
	GetItemText(gCurrentDialogID, editTextID, gNewValue[fieldNum]);
END;
```
```python
import vs

# Gets the text that is contained in the given componentID.
dialogID = 1
componentID = 2

result = vs.GetItemText(dialogID, componentID)
```

## See Also
[CreateEditText](CreateEditText.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
