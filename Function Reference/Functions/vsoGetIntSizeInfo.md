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

## Version
Availability: from Vectorworks 2023.3

## Category
* [Object Events](../Categories/Object%20Events.md)
