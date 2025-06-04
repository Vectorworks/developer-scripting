# EnableLBDragAndDrop

## Description
Enables list browser drag and drop.  Use SetLBDragDropColumn to set the drag and drop column.

```pascal
FUNCTION EnableLBDragAndDrop(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enable      : BOOLEAN): BOOLEAN;
```

```python
def vs.EnableLBDragAndDrop(dialogID, componentID, enable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enable|BOOLEAN|determines if drag and drop should be enabled|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
