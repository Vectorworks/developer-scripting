# vsoGetIntSizeInfo

## Description
Gets the parameter information needed for interactive sizeing.

```pascal
PROCEDURE vsoGetIntSizeInfo(
				message      : LONGINT;
				isz_index    : INTEGER;
				displayName  : STRING;
				currentValue : REAL;
				defaultValue : REAL;
				readOnly     : BOOLEAN;
				isSupported  : BOOLEAN);
```

```python
def vs.vsoGetIntSizeInfo(message, isz_index, displayName, currentValue, defaultValue, readOnly, isSupported):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|isz_index|INTEGER|   |
|displayName|STRING|   |
|currentValue|REAL|   |
|defaultValue|REAL|   |
|readOnly|BOOLEAN|   |
|isSupported|BOOLEAN|   |

## Examples
```pascal
vsoGetIntSizeInfo(1, 2, 'Example', 1.0, 2.0, TRUE, FALSE);
```
```python
import vs

# Gets the parameter information needed for interactive sizeing.
message = 'Hello Vectorworks'
isz_index = 1
displayName = 'Example'
currentValue = 1.0
defaultValue = 2.0
readOnly = True
isSupported = True

vs.vsoGetIntSizeInfo(message, isz_index, displayName, currentValue, defaultValue, readOnly, isSupported)
```

## Version
Availability: from Vectorworks 2023.3

## Category
* [Object Events](../Categories/Object%20Events.md)
