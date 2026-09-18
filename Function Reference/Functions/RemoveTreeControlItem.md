# RemoveTreeControlItem

## Description
Removes an item from a Layout Manager tree control.

```pascal
FUNCTION RemoveTreeControlItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nItemID      : INTEGER): BOOLEAN;
```

```python
def vs.RemoveTreeControlItem(nDialogID, nComponentID, nItemID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |

## Examples
```pascal
resultOK := RemoveTreeControlItem(1, 2, 3);
```
```python
import vs

# Removes an item from a Layout Manager tree control.
nDialogID = 1
nComponentID = 2
nItemID = 3

ok = vs.RemoveTreeControlItem(nDialogID, nComponentID, nItemID)
if ok:
    vs.Message('RemoveTreeControlItem succeeded')
else:
    vs.Message('RemoveTreeControlItem failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
