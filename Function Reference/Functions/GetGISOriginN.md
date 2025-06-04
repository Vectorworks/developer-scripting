# GetGISOriginN

## Description
Get geographical origin getting it from the document if the current layer is not georeferenced.

```pascal
FUNCTION GetGISOriginN(
				VAR outLat          : REAL;
				VAR outLon          : REAL;
				VAR outAngleToNorth : REAL): BOOLEAN;
```

```python
def vs.GetGISOriginN():
    return (BOOLEAN, outLat, outLon, outAngleToNorth)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outLat|REAL|   |
|outLon|REAL|   |
|outAngleToNorth|REAL|   |

## Version
Availability: from Vectorworks 2020

## Category
* [GIS](../Categories/GIS.md)
