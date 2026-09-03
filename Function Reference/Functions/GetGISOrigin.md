# GetGISOrigin

## Description
Get geographical origin.

```pascal
FUNCTION GetGISOrigin(
				VAR outLat          : REAL;
				VAR outLon          : REAL;
				VAR outAngleToNorth : REAL): BOOLEAN;
```

```python
def vs.GetGISOrigin():
    return (BOOLEAN, outLat, outLon, outAngleToNorth)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outLat|REAL|   |
|outLon|REAL|   |
|outAngleToNorth|REAL|   |

## Examples
```pascal
resultOK := GetGISOrigin(1.0, 2.0, 0.5);
```
```python
import vs

# Get geographical origin.
ok, outLat, outLon, outAngleToNorth = vs.GetGISOrigin()
vs.Message('GetGISOrigin returned: ' + str((ok, outLat, outLon, outAngleToNorth)))
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
