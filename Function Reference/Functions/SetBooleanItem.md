# SetBooleanItem

## Description
Selects or deselects the specified check box or radio button.

```pascal
PROCEDURE SetBooleanItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				setState    : BOOLEAN);
```

```python
def vs.SetBooleanItem(dialogID, componentID, setState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the radio or checkbox button component.|
|setState|BOOLEAN|The selection state to set for the given component.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
