# EnableTextEdit

## Description
Enables text editing for the given component.

```pascal
PROCEDURE EnableTextEdit(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				editableState : BOOLEAN);
```

```python
def vs.EnableTextEdit(dialogID, componentID, editableState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the text component.|
|editableState|BOOLEAN|True if this text component should be editable, false otherwise.|

## Examples
```pascal
EnableTextEdit(1, 2, TRUE);
```
```python
import vs

# Enables text editing for the given component.
dialogID = 1
componentID = 2
editableState = True

vs.EnableTextEdit(dialogID, componentID, editableState)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
