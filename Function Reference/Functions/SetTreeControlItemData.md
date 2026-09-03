# SetTreeControlItemData

## Description
Sets the user data of the specified item from a tree control.

```pascal
PROCEDURE SetTreeControlItemData(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nItemID      : INTEGER;
				nUserData    : LONGINT);
```

```python
def vs.SetTreeControlItemData(nDialogID, nComponentID, nItemID, nUserData):
    return None
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
SetTreeControlItemData(1, 2, 3, 10);
```
```python
import vs

# Sets the user data of the specified item from a tree control.
nDialogID = 1
nComponentID = 2
nItemID = 3
nUserData = 10

vs.SetTreeControlItemData(nDialogID, nComponentID, nItemID, nUserData)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
