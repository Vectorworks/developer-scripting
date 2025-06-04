# GetTreeControlItemText

## Description
Retrieves the item text of the specified item from a tree control.

```pascal
FUNCTION GetTreeControlItemText(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nItemID      : INTEGER;
				VAR itemText : STRING): BOOLEAN;
```

```python
def vs.GetTreeControlItemText(nDialogID, nComponentID, nItemID):
    return (BOOLEAN, itemText)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |
|itemText|STRING|   |

## Version
Availability: from Vectorworks 2011

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
