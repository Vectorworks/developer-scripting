# ClipPolygon

## Description
Same as [[VS:IntersectSurface]], but improves performance by first checking to see if hClipper is within the bounding box of hPolygon before calling IntersectSurface.

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

## Version
Availability: from Vectorworks 2014

## Category
* Graphic Calculation

