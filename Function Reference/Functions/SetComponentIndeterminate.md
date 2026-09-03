# SetComponentIndeterminate

## Description
Determines if the specified Layout Manager attribute control (line, weight, color, etc) should be set to the third, indeterminate state.

```pascal
FUNCTION SetComponentIndeterminate(
				nDialogID           : LONGINT;
				nComponentID        : LONGINT;
				bIndeterminateState : BOOLEAN): BOOLEAN;
```

```python
def vs.SetComponentIndeterminate(nDialogID, nComponentID, bIndeterminateState):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|bIndeterminateState|BOOLEAN|   |

## Examples
```pascal
resultOK := SetComponentIndeterminate(1, 2, TRUE);
```
```python
import vs

# Determines if the specified Layout Manager attribute control (line, weight,
# color, etc) should be set to the third, indeterminate state.
nDialogID = 1
nComponentID = 2
bIndeterminateState = True

ok = vs.SetComponentIndeterminate(nDialogID, nComponentID, bIndeterminateState)
if ok:
    vs.Message('SetComponentIndeterminate succeeded')
else:
    vs.Message('SetComponentIndeterminate failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
