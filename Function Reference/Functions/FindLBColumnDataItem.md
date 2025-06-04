# FindLBColumnDataItem

## Description
Finds the column data item with the specified text.

```pascal
FUNCTION FindLBColumnDataItem(
				dialogID                : LONGINT;
				componentID             : LONGINT;
				columnIndex             : INTEGER;
				itemString              : STRING;
				VAR columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.FindLBColumnDataItem(dialogID, componentID, columnIndex, itemString):
    return (BOOLEAN, columnDataItemIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|itemString|STRING|the text to find|
|columnDataItemIndex|INTEGER|the index at which the text was found|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
