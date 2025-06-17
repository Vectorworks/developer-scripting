# OffsetPolyN

## Description
Offsets a polygon or polyline. Uses Parasolid to do it. Equivalent of Voronoy based OffsetPoly.

```pascal
FUNCTION OffsetPolyN(
				h              : HANDLE;
				offsetDistance : REAL;
				smoothCorners  : BOOLEAN): HANDLE;
```

```python
def vs.OffsetPolyN(h, offsetDistance, smoothCorners):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|offsetDistance|REAL|   |
|smoothCorners|BOOLEAN|   |

## Remarks
(*\_c\_*, 2020): 
* smoothCorners will create rounded corners
* there is a suppression of collinear vertexes from the original object, so the resulting poly doesn't necessarily have the same count of vertexes.

(*\_c\_*, 2011): It outputs a polygon (Type 5), polyline (Type 21) or a group (Type 11), according to the offset geometry and eventual intersections.
OffsetPolyN fails:
* on holes, they are ignored
* used from inside plug-in objects: deselects the object instance on drawing at each run, compelling the user to re-select (tested from VW 2011 through 2014, also in 2016).

## See Also
Similar calls:
* [OffsetPoly](OffsetPoly.md)
* [OffsetHandle](OffsetHandle.md)

## Version
Availability: from Vectorworks 2009

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
