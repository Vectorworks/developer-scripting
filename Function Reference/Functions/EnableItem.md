# EnableItem

## Description
Sets the enable state of a dialog item.

```pascal
PROCEDURE EnableItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enableState : BOOLEAN);
```

```python
def vs.EnableItem(dialogID, componentID, enableState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component to enable or disable given the state.|
|enableState|BOOLEAN|True if the component should be enabled, false otherwise.|

## Examples
```pascal
7: BEGIN
	GetBooleanItem(dialogID, 7, tmpBool);
	EnableItem(dialogID, 6, NOT tmpBool);
   END;

SetItemText(dialogID, 6, Num2Str (0, nSegs));
EnableItem(dialogID, 6, (method = 1));

BEGIN
	EnableItem(gCurrentDialogID, 3, backV [gDialogNum]);
	EnableItem(gCurrentDialogID, 4, nextV [gDialogNum]);
END;
```
```python
import vs

# Sets the enable state of a dialog item.
dialogID = 1
componentID = 2
enableState = True

vs.EnableItem(dialogID, componentID, enableState)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
