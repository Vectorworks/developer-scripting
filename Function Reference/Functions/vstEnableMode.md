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

## Examples
```pascal
{kToolPointAdded}
{	Fixed BUG 57175 by disabling the mode group while colecting tool points}
100: BEGIN
	vstEnableMode(1, FALSE);
END;
```
```python
import vs

# Enables or disables the specified mode.
inModeNumber = 0
inEnable = True

vs.vstEnableMode(inModeNumber, inEnable)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
