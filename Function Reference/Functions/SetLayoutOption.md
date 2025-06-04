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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
