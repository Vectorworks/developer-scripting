# vstGetDataString

## Description
Gets tool data.

```pascal
PROCEDURE vstGetDataString(
				inDataID    : LONGINT;
				VAR outData : DYNARRAY [] OF CHAR;
				VAR result  : BOOLEAN);
```

```python
def vs.vstGetDataString(inDataID):
    return (outData, result)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inDataID|LONGINT|   |
|outData|DYNARRAY [] OF CHAR|Output parameter.|
|result|BOOLEAN|Output parameter.|

## Remarks
Use a STRING rather than a DYNARRAY [] OF CHAR.  Currently DYNARRAY will cause VW to crash. (VW 2010)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
