# SetDocGeoRefByUsrOrg

## Description
Use the current user origin and the specified coordinate system (EPSG) to calculate the adjust internal origin's latitude/longitude.

```pascal
PROCEDURE SetDocGeoRefByUsrOrg(EPSG : INTEGER);
```

```python
def vs.SetDocGeoRefByUsrOrg(EPSG):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|EPSG|INTEGER|   |

## Examples
```pascal
SetDocGeoRefByUsrOrg(1);
```
```python
import vs

# Use the current user origin and the specified coordinate system (EPSG) to
# calculate the adjust internal origin's latitude/longitude.
EPSG = 1

vs.SetDocGeoRefByUsrOrg(EPSG)
```

## Version
Availability: from Vectorworks 2021

## Category
* [GIS](../Categories/GIS.md)
