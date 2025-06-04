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

## See Also
[CreateEditText|CreateEditText](CreateEditText|CreateEditText.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
