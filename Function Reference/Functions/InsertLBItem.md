# InsertLBItem

## Description
Insert an item into the specified list browser control. Returns the index of the created item.

```pascal
FUNCTION InsertLBItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER;
				itemString  : STRING): INTEGER;
```

```python
def vs.InsertLBItem(dialogID, componentID, itemIndex, itemString):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|index at which the item is to be inserted|
|itemString|STRING|text to set for item|

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
