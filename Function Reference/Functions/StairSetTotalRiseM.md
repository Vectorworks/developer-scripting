# StairSetTotalRiseM

## Description
Sets total rise of stair - not recommended for use as stair might end up with inconsistent and contradictory parameters.

```pascal
FUNCTION StairSetTotalRiseM(
				stair     : HANDLE;
				TotalRise : REAL): BOOLEAN;
```

```python
def vs.StairSetTotalRiseM(stair, TotalRise):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|TotalRise|REAL|   |

## Examples
```pascal
resultOK := StairSetTotalRiseM(stair, 1.0);
```
```python
import vs

# Sets total rise of stair - not recommended for use as stair might end up
# with inconsistent and contradictory parameters.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer
TotalRise = 1.0

ok = vs.StairSetTotalRiseM(stair, TotalRise)
if ok:
    vs.Message('StairSetTotalRiseM succeeded')
else:
    vs.Message('StairSetTotalRiseM failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
