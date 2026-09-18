# OffsetPoly

## Description
Offsets a polygon or polyline. Must handle open &amp; closed polys. A positive distance offsets to the outside; negative to the inside. Should remove self-intersecting segments from the result. Should support &quot;smooth&quot; vs. &quot;sharp&quot; offsets.

```pascal
FUNCTION OffsetPoly(
				h                      : HANDLE;
				offsetDistance         : REAL;
				numberOfOffsets        : INTEGER;
				consolidateVertices    : BOOLEAN;
				sharpCorners           : BOOLEAN;
				conversionRes          : INTEGER;
				consolidationTolerance : REAL): HANDLE;
```

```python
def vs.OffsetPoly(h, offsetDistance, numberOfOffsets, consolidateVertices, sharpCorners, conversionRes, consolidationTolerance):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|offsetDistance|REAL|   |
|numberOfOffsets|INTEGER|   |
|consolidateVertices|BOOLEAN|   |
|sharpCorners|BOOLEAN|   |
|conversionRes|INTEGER|   |
|consolidationTolerance|REAL|   |

## Remarks
(*\_c\_*, 2011): The routine was introduced undocumented by VW10 (2005), then made public by VW17 (2012).

OffsetPoly fails:
* on holes, they are ignored
* when by an offset less than 1 unit: it copies in place, instead of offsetting (tested from VW 2011 through 2014). For example:
:* Units meter, offset 1m > succeeds
:* Units meter, offset 0.9m > fails
:* Units cm, offset 1cm > succeeds
:* Units cm, offset 0.9cm > fails

## Examples
```pascal
tempPolyH := MakePolygon(shadowH);
{use the original polygon when there is no Custom Roof}
IF (pOverhang > 0) AND (NOT(pCustom_Roof)) THEN
dpathHandle := OffsetPoly(tempPolyH ,pOverhang,1,TRUE,TRUE,kRez,0.25")
ELSE
	BEGIN
		dpathHandle := CreateDuplicateObject(tempPolyH,NIL);
	END;

BEGIN
BaseLine := OffsetPoly(hPathObj,gOffset, 1, FALSE, TRUE, kConversionRes, .001);
IF IsPolyClosed(hPathObj) THEN
	BEGIN
	GetPolylineVertex(BaseLine,1,x1,y1,vertType,arcRad);
	IF vertType = 0 THEN

	for cnt := 1 to vertCnt DO AddPoint(left[cnt].x, left[cnt].y);
	for cnt := vertCnt DOWNTO 1 DO AddPoint(rght[cnt].x, rght[cnt].y);
EndPoly;
h := LNewObj;
roadPoly := OffsetPoly(h, .001", 1, FALSE, TRUE, 1, 1");
DelObj(h);
```
```python
import vs

# Offsets a polygon or polyline.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
offsetDistance = 1.0
numberOfOffsets = 5
consolidateVertices = True
sharpCorners = True
conversionRes = 1
consolidationTolerance = 1.0

objHandle = vs.OffsetPoly(h, offsetDistance, numberOfOffsets, consolidateVertices, sharpCorners, conversionRes, consolidationTolerance)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [14. Polygon Inward / Outward Offset](ai%20examples/14_PolygonInwardOffset.md)

## See Also
Similar calls:
* [OffsetPolyN](OffsetPolyN.md)
* [OffsetHandle](OffsetHandle.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
