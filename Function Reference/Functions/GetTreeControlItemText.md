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

## Examples
```pascal
resultOK := GetTreeControlItemText(1, 2, 3, 'Example');
```
```python
import vs

# Retrieves the item text of the specified item from a tree control.
nDialogID = 1
nComponentID = 2
nItemID = 3

ok, itemText = vs.GetTreeControlItemText(nDialogID, nComponentID, nItemID)
vs.Message('GetTreeControlItemText returned: ' + str((ok, itemText)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
