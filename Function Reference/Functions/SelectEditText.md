# SelectEditText

## Description
Activates the given text component and selects its text.
[MaKro] Hint: Can be used to set the cursor at end of text when used in combination with VS:DeselectEditText

```pascal
PROCEDURE SelectEditText(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.SelectEditText(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component that is to be activated and selected.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
