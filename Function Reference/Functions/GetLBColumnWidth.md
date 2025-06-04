# GetLBColumnWidth

## Description
Gets the width of the specified column in the specified list browser control.

```pascal
FUNCTION GetLBColumnWidth(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				VAR width   : INTEGER): BOOLEAN;
```

```python
def vs.GetLBColumnWidth(dialogID, componentID, columnIndex):
    return (BOOLEAN, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column from which to get the width|
|width|INTEGER|width of the column|

## Version
Availability: from Vectorworks14.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
