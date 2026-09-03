# StairSetWFlight1M

## Description
Sets width of stair - not recommended for use as stair might end up with inconsistent and contradictory parameters.

```pascal
FUNCTION StairSetWFlight1M(
				stair              : HANDLE;
				WidthOfFirstFlight : REAL): BOOLEAN;
```

```python
def vs.StairSetWFlight1M(stair, WidthOfFirstFlight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|WidthOfFirstFlight|REAL|   |

## Examples
```pascal
resultOK := StairSetWFlight1M(stair, 1.0);
```
```python
import vs

# Sets width of stair - not recommended for use as stair might end up with
# inconsistent and contradictory parameters.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer
WidthOfFirstFlight = 2.0

ok = vs.StairSetWFlight1M(stair, WidthOfFirstFlight)
if ok:
    vs.Message('StairSetWFlight1M succeeded')
else:
    vs.Message('StairSetWFlight1M failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
