# vstEnableMode

## Description
Enables or disables the specified mode.  Modes are numbered starting from 1 in the order they were added into the mode bar.  Passing enable as false disables the mode; true enables it.

```pascal
PROCEDURE vstEnableMode(
				inModeNumber : INTEGER;
				inEnable     : BOOLEAN);
```

```python
def vs.vstEnableMode(inModeNumber, inEnable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inModeNumber|INTEGER|   |
|inEnable|BOOLEAN|   |

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
