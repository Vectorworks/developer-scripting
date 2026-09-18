# RemoveAllLBColumnDataItems

## Description
Removes all column data items.

```pascal
PROCEDURE RemoveAllLBColumnDataItems(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER);
```

```python
def vs.RemoveAllLBColumnDataItems(dialogID, componentID, columnIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|

## Examples
```pascal
RemoveAllLBColumnDataItems(1, 2, 3);
```
```python
import vs

# Removes all column data items.
dialogID = 1
componentID = 2
columnIndex = 1

vs.RemoveAllLBColumnDataItems(dialogID, componentID, columnIndex)
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
