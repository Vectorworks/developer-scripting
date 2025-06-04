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

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
