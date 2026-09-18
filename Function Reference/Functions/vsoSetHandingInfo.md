# vsoSetHandingInfo

## Description
Sets the Handing parameter values.

```pascal
PROCEDURE vsoSetHandingInfo(
				message         : LONGINT;
				isz_index       : INTEGER;
				VAR newValue    : REAL;
				VAR isSupported : BOOLEAN);
```

```python

def vs.vsoSetHandingInfo(message, isz_index):
    return (newValue, isSupported)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT||
|isz_index|INTEGER||
|newValue|REAL||
|isSupported|BOOLEAN||

## Examples
```pascal
vsoSetHandingInfo(1, 2, 1.0, TRUE);
```
```python
import vs

# Sets the Handing parameter values.
message = 'Hello Vectorworks'
isz_index = 1

newValue, isSupported = vs.vsoSetHandingInfo(message, isz_index)
vs.Message('vsoSetHandingInfo returned: ' + str((newValue, isSupported)))
```

## Version
Availability: from Vectorworks 2024

## Category
* [Object Events](../Categories/Object Events.md)
