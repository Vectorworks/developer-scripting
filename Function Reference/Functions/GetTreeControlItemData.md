# GetTreeControlItemData

## Description
Retrieves the user data of the specified item from a tree control.

```pascal
PROCEDURE GetTreeControlItemData(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nItemID       : INTEGER;
				VAR nUserData : LONGINT);
```

```python
def vs.GetTreeControlItemData(nDialogID, nComponentID, nItemID):
    return nUserData
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |
|nUserData|LONGINT|   |

## Examples
```pascal
GetTreeControlItemData(1, 2, 3, 10);
```
```python
import vs

# Retrieves the user data of the specified item from a tree control.
nDialogID = 1
nComponentID = 2
nItemID = 3

result = vs.GetTreeControlItemData(nDialogID, nComponentID, nItemID)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
