# LandmarkMatchSlope

## Description
Matches slope and contour angle information of a Landmark object to the specified 3D polygon.

```pascal
PROCEDURE LandmarkMatchSlope(
				h           : HANDLE;
				h3d         : HANDLE;
				landmarkObj : HANDLE);
```

```python
def vs.LandmarkMatchSlope(h, h3d, landmarkObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|h3d|HANDLE|   |
|landmarkObj|HANDLE|   |

## Examples
```pascal
LandmarkMatchSlope( h, h3D, gPluginObjH );
```
```python
import vs

# Matches slope and contour angle information of a Landmark object to the
# specified 3D polygon.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
h3d = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
landmarkObj = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.LandmarkMatchSlope(h, h3d, landmarkObj)
```

## Version
Availability: from Vectorworks 2016

## Category
* [Utility](../Categories/Utility.md)
