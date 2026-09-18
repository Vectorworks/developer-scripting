# vstGetModeValue

## Description
Returns the value of the specified mode.  Different mode types return values as follows:

*radio button:  Returns the number of the currently selected radio button (numbered left to right starting at 1.)
*checkbox: Returns 1 if the checkbox is checked, 0 if it is not.
*button:  Always returns 0.

```pascal
PROCEDURE vstGetModeValue(
				inModeGroup  : LONGINT;
				VAR outValue : LONGINT);
```

```python
def vs.vstGetModeValue(inModeGroup):
    return outValue
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inModeGroup|LONGINT|   |
|outValue|LONGINT|Output parameter.|

## Examples
```pascal
CASE modeGroup OF
	{insertion mode}
	1: BEGIN
		vstGetModeValue (1, modeValue_1);
		SetHelpMessage (modeValue_1);
		vstSetDataLong (kModeDataID_1, modeValue_1, result);
	END;

BEGIN
	vstGetModeValue( 1, modeValue );
	SetHelpMessage( modeValue );
	vstSetDataLong( kModeDataID, modeValue, result );
END;

kToolModeEventID: BEGIN
	vstGetModeValue (1, modeValue_1);
	vstGetModeValue (2, modeValue_2);
```
```python
import vs

# Returns the value of the specified mode.
inModeGroup = 0

result = vs.vstGetModeValue(inModeGroup)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
