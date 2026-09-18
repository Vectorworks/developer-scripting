# StairGetWFlight1M

## Description
Returns Width Of First Flight in meter or -1 in case of error.

```pascal
FUNCTION StairGetWFlight1M(stair : HANDLE): REAL;
```

```python
def vs.StairGetWFlight1M(stair):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultVal := StairGetWFlight1M(stair);
```
```python
import vs

# Returns Width Of First Flight in meter or -1 in case of error.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.StairGetWFlight1M(stair)
vs.Message('StairGetWFlight1M returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
