# vstGetDataReal

## Description
Gets tool data.

```pascal
PROCEDURE vstGetDataReal(
				inDataID    : LONGINT;
				VAR outData : REAL;
				VAR result  : BOOLEAN);
```

```python
def vs.vstGetDataReal(inDataID):
    return (outData, result)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|outData|REAL|Output parameter.|
|result|BOOLEAN|Output parameter.|

## Examples
```pascal
vstGetDataReal(1, 1.0, TRUE);
```
```python
import vs

# Gets tool data.
inDataID = 1

outData, result = vs.vstGetDataReal(inDataID)
vs.Message('vstGetDataReal returned: ' + str((outData, result)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
