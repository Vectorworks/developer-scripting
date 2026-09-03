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

## Examples
```pascal
resultOK := VWCoordToGeogN(1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Get geographical coordinates of a point (latitude and longitude) getting it
# from the document if the current layer is not georeferenced.
inCoordX = 1.0
inCoordY = 2.0

ok, outLat, outLon = vs.VWCoordToGeogN(inCoordX, inCoordY)
vs.Message('VWCoordToGeogN returned: ' + str((ok, outLat, outLon)))
```

## Version
Availability: from Vectorworks 2020

## Category
* [GIS](../Categories/GIS.md)
