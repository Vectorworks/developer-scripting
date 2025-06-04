# SetLBSortColumn

## Description
Sets the specified column as the sort column in the specified list browser control.

```pascal
PROCEDURE SetLBSortColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				isAscending : BOOLEAN);
```

```python
def vs.SetLBSortColumn(dialogID, componentID, columnIndex, isAscending):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|
|isAscending|BOOLEAN|determines if the sort should be ascending or descending|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
