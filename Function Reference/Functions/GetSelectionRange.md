# GetSelectionRange

## Description
Returns the range of the current selection for the specified control.

```pascal
PROCEDURE GetSelectionRange(
				dialogID     : LONGINT;
				controlID    : LONGINT;
				VAR startPos : INTEGER;
				VAR endPos   : INTEGER);
```

```python
def vs.GetSelectionRange(dialogID, controlID):
    return (startPos, endPos)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |
|startPos|INTEGER|   |
|endPos|INTEGER|   |

## Examples
```pascal
GetSelectionRange(1, 2, 3, 10);
```
```python
import vs

# Returns the range of the current selection for the specified control.
dialogID = 1
controlID = 2

startPos, endPos = vs.GetSelectionRange(dialogID, controlID)
vs.Message('GetSelectionRange returned: ' + str((startPos, endPos)))
```

## Version
Availability: from VectorWorks12.0.1

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
