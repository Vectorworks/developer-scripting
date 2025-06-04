# vstGetPt3D

## Description
Returns the point picked by the user at the specified index.

```pascal
PROCEDURE vstGetPt3D(
				inPtIndex : LONGINT;
				VAR outX  : REAL;
				VAR outY  : REAL;
				VAR outZ  : REAL;
				result    : BOOLEAN);
```

```python
def vs.vstGetPt3D(inPtIndex, result):
    return (outX, outY, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPtIndex|LONGINT|   |
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|outZ|REAL|Output parameter.|
|result|BOOLEAN|   |

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
