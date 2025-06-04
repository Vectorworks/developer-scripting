# vstSetDataLong

## Description
VSTs store persistent data between calls using vstSetDataLong and vstGetDataLong.

```pascal
PROCEDURE vstSetDataLong(
				inDataID   : LONGINT;
				inDataVal  : LONGINT;
				VAR result : BOOLEAN);
```

```python
def vs.vstSetDataLong(inDataID, inDataVal):
    return result
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|inDataVal|LONGINT|   |
|result|BOOLEAN|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
