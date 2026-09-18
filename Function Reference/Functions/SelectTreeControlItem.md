# SelectTreeControlItem

## Description
Selects the specified tree control item.

```pascal
PROCEDURE SelectTreeControlItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nItemID      : INTEGER);
```

```python
def vs.SelectTreeControlItem(nDialogID, nComponentID, nItemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |

## Examples
```pascal
SelectTreeControlItem(1, 2, 3);
```
```python
import vs

# Selects the specified tree control item.
nDialogID = 1
nComponentID = 2
nItemID = 3

vs.SelectTreeControlItem(nDialogID, nComponentID, nItemID)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
