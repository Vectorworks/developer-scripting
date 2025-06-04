# GetBooleanItem

## Description
Determines if a radio or checkbox button is selected or not.

```pascal
PROCEDURE GetBooleanItem(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				VAR outState : BOOLEAN);
```

```python
def vs.GetBooleanItem(dialogID, componentID):
    return outState
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the radio or checkbox button component.|
|outState|BOOLEAN|True if the button is selected, false otherwise.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
