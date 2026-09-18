# vsoGetHandingInfo

## Description
Gets the Handing parameter information.

```pascal
PROCEDURE vsoGetHandingInfo(
				message      : LONGINT;
				isz_index    : INTEGER;
				displayName  : STRING;
				currentValue : REAL;
				defaultValue : REAL;
				readOnly     : BOOLEAN;
				isSupported  : BOOLEAN);
```

```python

def vs.vsoGetHandingInfo(message, isz_index, displayName, currentValue, defaultValue, readOnly, isSupported):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT||
|isz_index|INTEGER||
|displayName|STRING||
|currentValue|REAL||
|defaultValue|REAL||
|readOnly|BOOLEAN||
|isSupported|BOOLEAN||

## Examples
```pascal
vsoGetHandingInfo(1, 2, 'Example', 1.0, 2.0, TRUE, FALSE);
```
```python
import vs

# Gets the Handing parameter information.
message = 'Hello Vectorworks'
isz_index = 1
displayName = 'Example'
currentValue = 1.0
defaultValue = 2.0
readOnly = True
isSupported = True

vs.vsoGetHandingInfo(message, isz_index, displayName, currentValue, defaultValue, readOnly, isSupported)
```

## Version
Availability: from Vectorworks 2024

## Category
* [Object Events](../Categories/Object Events.md)
