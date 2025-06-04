# vstGetDataLong

## Description
VSTs store persistent data between calls using vstSetDataLong and vstGetDataLong.

```pascal
PROCEDURE vstGetDataLong(
				inDataID    : LONGINT;
				VAR outData : LONGINT;
				VAR result  : BOOLEAN);
```

```python
def vs.vstGetDataLong(inDataID):
    return (outData, result)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|outData|LONGINT|Output parameter.|
|result|BOOLEAN|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
