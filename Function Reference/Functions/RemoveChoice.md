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

## Examples
```pascal
BEGIN
	FOR i := 1 TO numLines  DO
		RemoveChoice(dialogID, fieldID, 0);

BEGIN
	RemoveChoice(dlogID, 22, (i -1));
	i := i - 1;
END;

choicenum := choicenum + 1;
IF (choicestr <> kRecDefault) THEN BEGIN
	GetChoiceText(dlogID, 11, 1-1,  tempchoice);
	IF (tempchoice = kRecDefault) THEN BEGIN
		RemoveChoice(dlogID, 11, 1-1);
		EnableItem(dlogID, 1, TRUE);
		EnableItem(dlogID, 12, TRUE);
		SelectChoice(dlogID, 11, choicenum-1-1, TRUE);
	END;
```
```python
import vs

# Remove a menu item from a control that can display a menu.
dialogID = 1
componentID = 2
itemIndex = 1

vs.RemoveChoice(dialogID, componentID, itemIndex)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
