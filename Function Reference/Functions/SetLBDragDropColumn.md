# SetLBDragDropColumn

## Description
Sets the drag and drop column.

```pascal
FUNCTION SetLBDragDropColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetLBDragDropColumn(dialogID, componentID, columnIndex):
    return BOOLEAN
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
