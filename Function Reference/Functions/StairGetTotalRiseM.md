# StairGetTotalRiseM

## Description
Returns Total Rise in meter or -1 in case of error.

```pascal
FUNCTION StairGetTotalRiseM(stair : HANDLE): REAL;
```

```python
def vs.StairGetTotalRiseM(stair):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultVal := StairGetTotalRiseM(stair);
```
```python
import vs

# Returns Total Rise in meter or -1 in case of error.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.StairGetTotalRiseM(stair)
vs.Message('StairGetTotalRiseM returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
