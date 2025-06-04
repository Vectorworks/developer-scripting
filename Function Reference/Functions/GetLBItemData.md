# GetLBItemData

## Description
Retrieves the user data associated with the list browser item.

```pascal
PROCEDURE GetLBItemData(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nItemIndex    : INTEGER;
				nSubItemIndex : INTEGER;
				VAR nUserData : LONGINT);
```

```python
def vs.GetLBItemData(nDialogID, nComponentID, nItemIndex, nSubItemIndex):
    return nUserData
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemIndex|INTEGER|   |
|nSubItemIndex|INTEGER|   |
|nUserData|LONGINT|   |

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
