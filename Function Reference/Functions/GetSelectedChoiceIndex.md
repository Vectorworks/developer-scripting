# GetSelectedChoiceIndex

## Description
Gets the 0-based index of the selected choice.

```pascal
PROCEDURE GetSelectedChoiceIndex(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				startIndex           : INTEGER;
				VAR outSelectedIndex : INTEGER);
```

```python
def vs.GetSelectedChoiceIndex(dialogID, componentID, startIndex):
    return outSelectedIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|startIndex|INTEGER|The index at which to start looking for a selected item.|
|outSelectedIndex|INTEGER|The index of the selected item or -1 if there is no selected item.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
