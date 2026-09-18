# ExpandTreeControlItem

## Description
Expands or collapses the specified tree control item.

```pascal
PROCEDURE ExpandTreeControlItem(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nItemID      : INTEGER;
				bExpand      : BOOLEAN);
```

```python
def vs.ExpandTreeControlItem(nDialogID, nComponentID, nItemID, bExpand):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nItemID|INTEGER|   |
|bExpand|BOOLEAN|   |

## Examples
```pascal
ExpandTreeControlItem(1, 2, 3, TRUE);
```
```python
import vs

# Expands or collapses the specified tree control item.
nDialogID = 1
nComponentID = 2
nItemID = 3
bExpand = True

vs.ExpandTreeControlItem(nDialogID, nComponentID, nItemID, bExpand)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
