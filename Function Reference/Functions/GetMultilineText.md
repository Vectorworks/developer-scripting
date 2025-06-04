# GetMultilineText

## Description
Gets the text that is contained in the given componentID.

```pascal
PROCEDURE GetMultilineText(
				dialogID    : LONGINT;
				componentID : LONGINT;
				VAR text    : DYNARRAY[] of CHAR);
```

```python
def vs.GetMultilineText(dialogID, componentID):
    return text
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component that the text will be retrieved from.|
|text|DYNARRAY[] of CHAR|The text of the component.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
