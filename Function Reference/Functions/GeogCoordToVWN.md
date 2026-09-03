# GeogCoordToVWN

## Description
Get point in Vectorworks coordinates getting it from the document if the current layer is not georeferenced.

```pascal
FUNCTION GeogCoordToVWN(
				inLat        : REAL;
				inLon        : REAL;
				VAR outCoord : REAL): BOOLEAN;
```

```python
def vs.GeogCoordToVWN(inLat, inLon):
    return (BOOLEAN, outCoord)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inLat|REAL|   |
|inLon|REAL|   |
|outCoord|REAL|   |

## Examples
```pascal
resultOK := GeogCoordToVWN(1.0, 2.0, 0.5);
```
```python
import vs

# Get point in Vectorworks coordinates getting it from the document if the
# current layer is not georeferenced.
inLat = 1.0
inLon = 2.0

ok, outCoord = vs.GeogCoordToVWN(inLat, inLon)
vs.Message('GeogCoordToVWN returned: ' + str((ok, outCoord)))
```

## Version
Availability: from Vectorworks 2020

## Category
* [GIS](../Categories/GIS.md)
