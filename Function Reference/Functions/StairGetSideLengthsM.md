# StairGetSideLengthsM

## Description
Returns Lengths of sides of stair. All values are in meters. Returns -1 in case of error or for sides that don't exist.

```pascal
FUNCTION StairGetSideLengthsM(
				stair            : HANDLE;
				VAR LengthSide1M : REAL;
				VAR LengthSide2M : REAL;
				VAR LengthSide3M : REAL;
				VAR LengthSide4M : REAL;
				VAR LengthSide5M : REAL): BOOLEAN;
```

```python
def vs.StairGetSideLengthsM(stair):
    return (BOOLEAN, LengthSide1M, LengthSide2M, LengthSide3M, LengthSide4M, LengthSide5M)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|LengthSide1M|REAL|   |
|LengthSide2M|REAL|   |
|LengthSide3M|REAL|   |
|LengthSide4M|REAL|   |
|LengthSide5M|REAL|   |

## Examples
```pascal
resultOK := StairGetSideLengthsM(stair, 1.0, 2.0, 0.5, 1.5, 3.0);
```
```python
import vs

# Returns Lengths of sides of stair.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, LengthSide1M, LengthSide2M, LengthSide3M, LengthSide4M, LengthSide5M = vs.StairGetSideLengthsM(stair)
vs.Message('StairGetSideLengthsM returned: ' + str((ok, LengthSide1M, LengthSide2M, LengthSide3M, LengthSide4M, LengthSide5M)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
