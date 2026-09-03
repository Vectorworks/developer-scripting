# vsoSetIntSizeInfo

## Description
Sets the parameter values after interactive sizeing.

```pascal
PROCEDURE vsoSetIntSizeInfo(
				message         : LONGINT;
				isz_index       : INTEGER;
				VAR newValue    : REAL;
				VAR isSupported : BOOLEAN);
```

```python
def vs.vsoSetIntSizeInfo(message, isz_index):
    return (newValue, isSupported)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|isz_index|INTEGER|   |
|newValue|REAL|   |
|isSupported|BOOLEAN|   |

## Examples
```pascal
vsoSetIntSizeInfo(1, 2, 1.0, TRUE);
```
```python
import vs

# Sets the parameter values after interactive sizeing.
message = 'Hello Vectorworks'
isz_index = 1

newValue, isSupported = vs.vsoSetIntSizeInfo(message, isz_index)
vs.Message('vsoSetIntSizeInfo returned: ' + str((newValue, isSupported)))
```

## Version
Availability: from Vectorworks 2023.3

## Category
* [Object Events](../Categories/Object%20Events.md)
