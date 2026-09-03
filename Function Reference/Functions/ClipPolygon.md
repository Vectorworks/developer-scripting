# ClipPolygon

## Description
Same as [IntersectSurface](IntersectSurface.md), but improves performance by first checking to see if hClipper is within the bounding box of hPolygon before calling IntersectSurface.

```pascal
FUNCTION ClipPolygon(
				hPolygon : HANDLE;
				hClipper : HANDLE;
				dFuzz    : REAL): HANDLE;
```

```python
def vs.ClipPolygon(hPolygon, hClipper, dFuzz):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPolygon|HANDLE|   |
|hClipper|HANDLE|   |
|dFuzz|REAL|   |

## Examples
```pascal
resultH := ClipPolygon(hPolygon, hClipper, 1.0);
```
```python
import vs

# Same as IntersectSurface, but improves performance by first checking to see
# if hClipper is within the bounding box of hPolygon before calling
# IntersectSurface.
hPolygon = vs.FSActLayer()  # handle to the first selected object on the active layer
hClipper = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
dFuzz = 1.0

objHandle = vs.ClipPolygon(hPolygon, hClipper, dFuzz)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
