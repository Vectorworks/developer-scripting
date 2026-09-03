# Polygonize

## Description
Polygonize polylines and polygons.

```pascal
FUNCTION Polygonize(
				h                  : HANDLE;
				segmentationLength : REAL;
				polygonizeStraight : BOOLEAN): HANDLE;
```

```python
def vs.Polygonize(h, segmentationLength, polygonizeStraight):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|segmentationLength|REAL|   |
|polygonizeStraight|BOOLEAN|   |

## Examples
```pascal
BEGIN
	hPoly2 := Polygonize(hPoly, resolution, FALSE);
	DelObject(hPoly);
	PolygonizeAndDeleteOrig := hPoly2;
END;

BEGIN
	tempSegLength	:= segLength * ( 25.4 / GetPrefReal( 152 ) );
	h 				:= Polygonize( polyHandle, tempSegLength, true );
	polyHandle		:= h;
END;
```
```python
import vs

# Polygonize polylines and polygons.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
segmentationLength = 1.0
polygonizeStraight = True

objHandle = vs.Polygonize(h, segmentationLength, polygonizeStraight)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
