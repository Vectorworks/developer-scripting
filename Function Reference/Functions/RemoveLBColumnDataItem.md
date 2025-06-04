# RemoveLBColumnDataItem

## Description
Removes the specified column data item.

```pascal
FUNCTION RemoveLBColumnDataItem(
				dialogID            : LONGINT;
				componentID         : LONGINT;
				columnIndex         : INTEGER;
				columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.RemoveLBColumnDataItem(dialogID, componentID, columnIndex, columnDataItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|columnDataItemIndex|INTEGER|the column data item to remove|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
