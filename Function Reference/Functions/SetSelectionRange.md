# SetSelectionRange

## Description
Sets the range of the current selection for the specified control.

```pascal
PROCEDURE SetSelectionRange(
				dialogID  : LONGINT;
				controlID : LONGINT;
				startPos  : INTEGER;
				endPos    : INTEGER);
```

```python
def vs.SetSelectionRange(dialogID, controlID, startPos, endPos):
    return None
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
SetSelectionRange(1, 2, 3, 10);
```
```python
import vs

# Sets the range of the current selection for the specified control.
dialogID = 1
controlID = 2
startPos = 3
endPos = 10

vs.SetSelectionRange(dialogID, controlID, startPos, endPos)
```

## Version
Availability: from VectorWorks12.0.1

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
