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
([[User:CBM-c-|_c_]], 2011): The routine was introduced undocumented by VW10 (2005), then made public by VW17 (2012).

OffsetPoly fails:
* on holes, they are ignored
* when by an offset less than 1 unit: it copies in place, instead of offsetting (tested from VW 2011 through 2014). For example:
:* Units meter, offset 1m > succeeds
:* Units meter, offset 0.9m > fails
:* Units cm, offset 1cm > succeeds
:* Units cm, offset 0.9cm > fails

## See Also
Similar calls:
* [OffsetPolyN](OffsetPolyN.md)
* [OffsetHandle](OffsetHandle.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
