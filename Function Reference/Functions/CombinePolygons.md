# CombinePolygons

## Description
Combines two polygons.

```pascal
FUNCTION CombinePolygons(
				hPolygonA : HANDLE;
				hPolygonB : HANDLE;
				dFuzz     : REAL): HANDLE;
```

```python
def vs.CombinePolygons(hPolygonA, hPolygonB, dFuzz):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPolygonA|HANDLE|   |
|hPolygonB|HANDLE|   |
|dFuzz|REAL|   |

## Examples
```pascal
resultH := CombinePolygons(hPolygonA, hPolygonB, 1.0);
```
```python
import vs

# Combines two polygons.
hPolygonA = vs.FSActLayer()  # handle to the first selected object on the active layer
hPolygonB = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
dFuzz = 1.0

objHandle = vs.CombinePolygons(hPolygonA, hPolygonB, dFuzz)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
