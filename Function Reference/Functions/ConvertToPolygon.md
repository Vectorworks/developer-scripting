# ConvertToPolygon

## Description
Converts object to polygon.

```pascal
FUNCTION ConvertToPolygon(
				h          : HANDLE;
				resolution : INTEGER): HANDLE;
```

```python
def vs.ConvertToPolygon(h, resolution):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|resolution|INTEGER|   |

## Remarks
Notes: (RMullin - 2020 Mar 03)
- Setting "resolution" higher creates more vertices. Magic numbers for "resolution" are [0, 8, 16, 32, 64, 128, 256, 512].
  - Integer values between the numbers in this list generate duplicate results.
  - Values outside this range do not appear to affect the number of vertices generated.
- This function creates a duplicate object, so you don't have to duplicate the object beforehand if you want to retain the original object.
- If the original is selected, the duplicate will be selected, and vice versa.

## Examples
```pascal
IF convertion THEN BEGIN
	IF ( (gTdType = 4) OR ( (gTdType = 13) | (gTdType = 21) ) )  THEN BEGIN
		h1 := h;
		DelObject(h);
		h := ConvertToPolygon(h1, 64 );
	END;

{create 2D polygon that presents nurbs fence curve}
h4 := ConvertToPolygon( h1, 16 );

BEGIN
	SegmentHand := ConvertToPolygon( tempHand, 0.1 );
	numVerticesConv	:= 	GetVertNum( SegmentHand );
	{ FIND INTERSECTION between line from the center of the bounding box to the center of the polygonized segment and the polygonized segment itself}
	{ center to Segment center vector scaled}
	pt1.x := ( Xc1  - BoxCx1)*1000;
```
```python
import vs

# Converts object to polygon.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
resolution = 1

objHandle = vs.ConvertToPolygon(h, resolution)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
