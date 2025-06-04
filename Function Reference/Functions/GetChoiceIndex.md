# GetChoiceIndex

## Description
Finds the index of the given string in a layout manager list box or pull down menu. The index is zero based and is set to -1 if the item is not found.

```pascal
PROCEDURE GetChoiceIndex(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemText      : STRING;
				VAR itemIndex : INTEGER);
```

```python
def vs.GetChoiceIndex(dialogID, componentID, itemText):
    return itemIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|itemText|STRING|   |
|itemIndex|INTEGER|   |

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
