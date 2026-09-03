# vstSetDataReal

## Description
Sets tool data.

```pascal
PROCEDURE vstSetDataReal(
				inDataID   : LONGINT;
				inDataVal  : REAL;
				VAR result : BOOLEAN);
```

```python
def vs.vstSetDataReal(inDataID, inDataVal):
    return result
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|inDataVal|REAL|   |
|result|BOOLEAN|Output parameter.|

## Examples
```pascal
vstSetDataReal(1, 1.0, TRUE);
```
```python
import vs

# Sets tool data.
inDataID = 1
inDataVal = 1.0

result = vs.vstSetDataReal(inDataID, inDataVal)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
