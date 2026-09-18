# RefreshItem

## Description
Refreshes the specified item.

```pascal
PROCEDURE RefreshItem(
				liDialogID    : LONGINT;
				liComponentID : LONGINT);
```

```python
def vs.RefreshItem(liDialogID, liComponentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |

## Examples
```pascal
RefreshItem(1, 2);
```
```python
import vs

# Refreshes the specified item.
liDialogID = 1
liComponentID = 2

vs.RefreshItem(liDialogID, liComponentID)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
