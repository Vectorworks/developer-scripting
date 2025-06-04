# vstGetCurrPt3D

## Description
Returns the current location of the mouse.

```pascal
PROCEDURE vstGetCurrPt3D(
				VAR outX : REAL;
				VAR outY : REAL;
				VAR outZ : REAL;
				result   : BOOLEAN);
```

```python
def vs.vstGetCurrPt3D(result):
    return (outX, outY, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|outZ|REAL|Output parameter.|
|result|BOOLEAN|   |

## Remarks
In Python, the result boolean input variable doesn't seem to do anything.

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
