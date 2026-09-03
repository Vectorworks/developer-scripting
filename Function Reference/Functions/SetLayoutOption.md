# SetLayoutOption

## Description
Set options for a specific Layout Manager dialog.  For use by certain alert dialogs that want centered &quot;OK&quot; button.

```pascal
FUNCTION SetLayoutOption(
				dialogID : LONGINT;
				option   : INTEGER;
				value    : LONGINT): BOOLEAN;
```

```python
def vs.SetLayoutOption(dialogID, option, value):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|option|INTEGER|   |
|value|LONGINT|   |

## Examples
```pascal
resultOK := SetLayoutOption(1, 2, 3);
```
```python
import vs

# Set options for a specific Layout Manager dialog.
dialogID = 1
option = 2
value = 3

ok = vs.SetLayoutOption(dialogID, option, value)
if ok:
    vs.Message('SetLayoutOption succeeded')
else:
    vs.Message('SetLayoutOption failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
