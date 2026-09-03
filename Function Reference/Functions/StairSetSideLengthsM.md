# StairSetSideLengthsM

## Description
Sets side lengths of stair - not recommended for use as stair might end up with inconsistent and contradictory parameters.

```pascal
FUNCTION StairSetSideLengthsM(
				stair        : HANDLE;
				LengthSide1M : REAL;
				LengthSide2M : REAL;
				LengthSide3M : REAL;
				LengthSide4M : REAL;
				LengthSide5M : REAL): BOOLEAN;
```

```python
def vs.StairSetSideLengthsM(stair, LengthSide1M, LengthSide2M, LengthSide3M, LengthSide4M, LengthSide5M):
    return BOOLEAN
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
resultOK := StairSetSideLengthsM(stair, 1.0, 2.0, 0.5, 1.5, 3.0);
```
```python
import vs

# Sets side lengths of stair - not recommended for use as stair might end up
# with inconsistent and contradictory parameters.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer
LengthSide1M = 1.0
LengthSide2M = 1.0
LengthSide3M = 1.0
LengthSide4M = 1.0
LengthSide5M = 1.0

ok = vs.StairSetSideLengthsM(stair, LengthSide1M, LengthSide2M, LengthSide3M, LengthSide4M, LengthSide5M)
if ok:
    vs.Message('StairSetSideLengthsM succeeded')
else:
    vs.Message('StairSetSideLengthsM failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
