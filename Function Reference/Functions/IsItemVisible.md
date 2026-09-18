# IsItemVisible

## Description
Determines if the specified item is currently visible.

```pascal
FUNCTION IsItemVisible(
				nDialogID    : LONGINT;
				nComponentID : LONGINT): BOOLEAN;
```

```python
def vs.IsItemVisible(nDialogID, nComponentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |

## Examples
```pascal
resultOK := IsItemVisible(1, 2);
```
```python
import vs

# Determines if the specified item is currently visible.
nDialogID = 1
nComponentID = 2

ok = vs.IsItemVisible(nDialogID, nComponentID)
if ok:
    vs.Message('IsItemVisible succeeded')
else:
    vs.Message('IsItemVisible failed')
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
