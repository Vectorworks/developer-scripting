# RemoveChoice

## Description
Remove a menu item from a control that can display a menu.

```pascal
PROCEDURE RemoveChoice(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER);
```

```python
def vs.RemoveChoice(dialogID, componentID, itemIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the control that will have its menu item removed.|
|itemIndex|INTEGER|The zero-based index of the menu item to remove.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
