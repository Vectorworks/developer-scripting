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

## Version
Availability: from Vectorworks 2020

## Category
* [GIS](../Categories/GIS.md)
