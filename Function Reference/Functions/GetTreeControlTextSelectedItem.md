# GetTreeControlTextSelectedItem

## Description
Retrieves the item text of the selected item from a tree control.

```pascal
FUNCTION GetTreeControlTextSelectedItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				VAR itemText : STRING): BOOLEAN;
```

```python
def vs.GetTreeControlTextSelectedItem(nDialogID, nComponentID):
    return (BOOLEAN, itemText)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|itemText|STRING|   |

## Examples
```pascal
resultOK := GetTreeControlTextSelectedItem(1, 2, 'Example');
```
```python
import vs

# Retrieves the item text of the selected item from a tree control.
nDialogID = 1
nComponentID = 2

ok, itemText = vs.GetTreeControlTextSelectedItem(nDialogID, nComponentID)
vs.Message('GetTreeControlTextSelectedItem returned: ' + str((ok, itemText)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
