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

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
