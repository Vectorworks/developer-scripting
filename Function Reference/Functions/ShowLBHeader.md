# ShowLBHeader

## Description
Shows or hides header row for a list browser control in a dialog

```pascal
PROCEDURE ShowLBHeader(
				dialogID    : LONGINT;
				componentID : LONGINT;
				show        : BOOLEAN);
```

```python
def vs.ShowLBHeader(dialogID, componentID, show):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|show|BOOLEAN|   |

## Examples
```pascal
ShowLBHeader(1, 2, TRUE);
```
```python
import vs

# Shows or hides header row for a list browser control in a dialog.
dialogID = 1
componentID = 2
show = True

vs.ShowLBHeader(dialogID, componentID, show)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
