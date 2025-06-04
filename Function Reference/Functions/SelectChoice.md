# SelectChoice

## Description
Set the selection state of the given item in a control of choices.

```pascal
PROCEDURE SelectChoice(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER;
				selectState : BOOLEAN);
```

```python
def vs.SelectChoice(dialogID, componentID, itemIndex, selectState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|itemIndex|INTEGER|The index of the item to set the selection state for.|
|selectState|BOOLEAN|True if the item at the given index should be selected. False otherwise.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
