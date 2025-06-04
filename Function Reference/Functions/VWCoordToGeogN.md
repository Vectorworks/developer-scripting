# VWCoordToGeogN

## Description
Get geographical coordinates of a point (latitude and longitude) getting it from the document if the current layer is not georeferenced.

```pascal
FUNCTION VWCoordToGeogN(
				inCoordX   : REAL;
				inCoordY   : REAL;
				VAR outLat : REAL;
				VAR outLon : REAL): BOOLEAN;
```

```python
def vs.VWCoordToGeogN(inCoordX, inCoordY):
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
Availability: from Vectorworks 2020

## Category
* [GIS](../Categories/GIS.md)
