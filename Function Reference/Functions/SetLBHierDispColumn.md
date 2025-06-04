# SetLBHierDispColumn

## Description
This function sets which column to display hierarchically in a list browser. This will only work on a text column. Items with dashes in the string value for the hierarchical column will be displayed hierarchically. This will work on items already entered. When new items are entered, this will need to be called again.

```pascal
PROCEDURE SetLBHierDispColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnID    : INTEGER);
```

```python
def vs.SetLBHierDispColumn(dialogID, componentID, columnID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|
|columnID|INTEGER|The index of the hierarchical column.|

## See Also
VS Functions:
[EnableLBHierDisplay](EnableLBHierDisplay.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
