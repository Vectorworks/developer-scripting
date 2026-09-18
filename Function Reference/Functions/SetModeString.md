# SetModeString

## Description
Sets the mode string to the given parameter

```pascal
PROCEDURE SetModeString(messageStr : STRING);
```

```python
def vs.SetModeString(messageStr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|messageStr|STRING|   |

## Examples
```pascal
BEGIN
	SetModeString(Message1);
	IF (GetName(GetRecord(theHoist,1)) = kHoistPIOName) THEN
		ChecObjectCallback := TRUE
	ELSE
		ChecObjectCallback := FALSE;
```
```python
import vs

# Sets the mode string to the given parameter.
messageStr = 'Hello Vectorworks'

vs.SetModeString(messageStr)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
