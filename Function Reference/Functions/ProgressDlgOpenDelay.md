# ProgressDlgOpenDelay

## Description
Show a progress dialog that doesn't interrupt the script. The dialog will be displaed after specified dealy time (in miliseconds). ProgressDlgClose must be used to close the dialog.

```pascal
PROCEDURE ProgressDlgOpenDelay(
				title     : STRING;
				canCancel : BOOLEAN;
				delaySec  : INTEGER);
```

```python
def vs.ProgressDlgOpenDelay(title, canCancel, delaySec):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|title|STRING|   |
|canCancel|BOOLEAN|   |
|delaySec|INTEGER|   |

## Examples
```pascal
ProgressDlgOpenDelay('Example', TRUE, 1);
```
```python
import vs

# Show a progress dialog that doesn't interrupt the script.
title = 'Example'
canCancel = True
delaySec = 1

vs.ProgressDlgOpenDelay(title, canCancel, delaySec)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Utility](../Categories/Utility.md)
