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

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
