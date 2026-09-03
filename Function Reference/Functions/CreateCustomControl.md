# CreateCustomControl

## Description
Creates a layout manager control in a VectorScript to be used in conjunction with GS_OverrideControl in an external dialog handler.

```pascal
PROCEDURE CreateCustomControl(
				dialogID    : LONGINT;
				componentID : LONGINT;
				iWidth      : INTEGER;
				iHeight     : INTEGER);
```

```python
def vs.CreateCustomControl(dialogID, componentID, iWidth, iHeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iWidth|INTEGER|   |
|iHeight|INTEGER|   |

## Examples
```pascal
CreateCustomControl(1, 2, 3, 10);
```
```python
import vs

# Creates a layout manager control in a VectorScript to be used in
# conjunction with GS_OverrideControl in an external dialog handler.
dialogID = 1
componentID = 2
iWidth = 3
iHeight = 10

vs.CreateCustomControl(dialogID, componentID, iWidth, iHeight)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks 13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
