# GeogCoordToVW

## Description
Get point in Vectorworks coordinates.

```pascal
FUNCTION GeogCoordToVW(
				inLat         : REAL;
				inLon         : REAL;
				VAR outCoordX : REAL;
				VAR outCoordY : REAL): BOOLEAN;
```

```python
def vs.GeogCoordToVW(inLat, inLon):
    return (BOOLEAN, outCoord)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inLat|REAL|   |
|inLon|REAL|   |
|outCoordX|REAL|   |
|outCoordY|REAL|   |

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
