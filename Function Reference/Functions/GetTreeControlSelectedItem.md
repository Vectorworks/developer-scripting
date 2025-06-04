# GetTreeControlSelectedItem

## Description
Retrieves the itemID of the selected item from a Layout Manager tree control.

```pascal
FUNCTION GetTreeControlSelectedItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				VAR nItemID  : INTEGER): BOOLEAN;
```

```python
def vs.GetTreeControlSelectedItem(nDialogID, nComponentID):
    return (BOOLEAN, nItemID)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
