# FindLBColumnItem

## Description
Finds the column item with the specified text.

```pascal
FUNCTION FindLBColumnItem(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				columnIndex   : INTEGER;
				itemString    : STRING;
				VAR itemIndex : INTEGER): BOOLEAN;
```

```python
def vs.FindLBColumnItem(dialogID, componentID, columnIndex, itemString):
    return (BOOLEAN, itemIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|itemString|STRING|the text to find|
|itemIndex|INTEGER|the index at which the text was found|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
