# GetChoiceText

## Description
Using the index, gets the text of the menu item of the given component.

```pascal
PROCEDURE GetChoiceText(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				VAR itemText : STRING);
```

```python
def vs.GetChoiceText(dialogID, componentID, itemIndex):
    return itemText
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the control that contains the menu items from which the text will be retrieved from.|
|itemIndex|INTEGER|The item index that contains the desired text.|
|itemText|STRING|The text of the item.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
