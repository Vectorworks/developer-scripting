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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
