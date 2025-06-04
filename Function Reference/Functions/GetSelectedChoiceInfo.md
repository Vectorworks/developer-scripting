# GetSelectedChoiceInfo

## Description
Gets the index of the selected item and the text of the selected item in a menu.

```pascal
PROCEDURE GetSelectedChoiceInfo(
				dialogID                  : LONGINT;
				componentID               : LONGINT;
				startIndex                : INTEGER;
				VAR outSelectedIndex      : INTEGER;
				VAR outSelectedChoiceText : STRING);
```

```python
def vs.GetSelectedChoiceInfo(dialogID, componentID, startIndex):
    return (outSelectedIndex, outSelectedChoiceText)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|startIndex|INTEGER|The index at which to start looking for a selected item.|
|outSelectedIndex|INTEGER|The index of the selected item or -1 if there is no selected item.|
|outSelectedChoiceText|STRING|The text of the selected item if it was found, otherwise this parameter is unchanged from when this function was called.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
