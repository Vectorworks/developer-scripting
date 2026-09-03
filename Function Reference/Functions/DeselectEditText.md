# DeselectEditText

## Description
Deselects all text in the specified edit control.

```pascal
PROCEDURE DeselectEditText(
				dialogID  : LONGINT;
				controlID : LONGINT);
```

```python
def vs.DeselectEditText(dialogID, controlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |

## Examples
```pascal
DeselectEditText(1, 2);
```
```python
import vs

# Deselects all text in the specified edit control.
dialogID = 1
controlID = 2

vs.DeselectEditText(dialogID, controlID)
```

## Version
Availability: from VectorWorks12.0.1

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
