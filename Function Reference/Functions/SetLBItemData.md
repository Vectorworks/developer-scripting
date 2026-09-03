# SetLBItemData

## Description
Sets the user data associated with the list browser item.

```pascal
PROCEDURE SetLBItemData(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nItemIndex    : INTEGER;
				nSubItemIndex : INTEGER;
				nUserData     : LONGINT);
```

```python
def vs.SetLBItemData(nDialogID, nComponentID, nItemIndex, nSubItemIndex, nUserData):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemIndex|INTEGER|   |
|nSubItemIndex|INTEGER|   |
|nUserData|LONGINT|   |

## Examples
```pascal
SetLBItemData(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the user data associated with the list browser item.
nDialogID = 1
nComponentID = 2
nItemIndex = 1
nSubItemIndex = 1
nUserData = 3

vs.SetLBItemData(nDialogID, nComponentID, nItemIndex, nSubItemIndex, nUserData)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
