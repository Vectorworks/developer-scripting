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

## Version
Availability: from Vectorworks 2023.3

## Category
* [Object Events](../Categories/Object%20Events.md)
