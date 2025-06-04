# GetLBColumnSortState

## Description
Gets the column sort state. Returns 0: not sorted; -1: 1..n sorted; 1: n..1 sorted.

```pascal
FUNCTION GetLBColumnSortState(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): INTEGER;
```

```python
def vs.GetLBColumnSortState(dialogID, componentID, columnIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
