# GetChoiceCount

## Description
Gets the number of items in the component that contains the choices.

```pascal
PROCEDURE GetChoiceCount(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				VAR outCount : INTEGER);
```

```python
def vs.GetChoiceCount(dialogID, componentID):
    return outCount
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the component that contains the choices.|
|outCount|INTEGER|The number of items in the component.|

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
