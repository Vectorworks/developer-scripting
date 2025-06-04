# VWCoordToGeog

## Description
Get geographical coordinates of a point (latitude and longitude).

```pascal
FUNCTION VWCoordToGeog(
				inCoordX   : REAL;
				inCoordY   : REAL;
				VAR outLat : REAL;
				VAR outLon : REAL): BOOLEAN;
```

```python
def vs.VWCoordToGeog(inCoordX, inCoordY):
    return (BOOLEAN, outLat, outLon)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inCoordX|REAL|   |
|inCoordY|REAL|   |
|outLat|REAL|   |
|outLon|REAL|   |

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
