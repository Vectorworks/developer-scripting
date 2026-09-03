# ConvertToPolyline

## Description
Converts any enclosed shape (circle, rectangle, ellipse, etc.) into a polygon or polyline. Does not polygonalize.

```pascal
FUNCTION ConvertToPolyline(h : HANDLE): HANDLE;
```

```python
def vs.ConvertToPolyline(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
PrepRelatedObjectForChange(tempH1);
selHandles[TmpIndex] := ConvertToPolyline(selHandles[TmpIndex]);

BEGIN
	rectH := polyH;
	SetDSelect (rectH);
	polyH := ConvertToPolyline( HDuplicate( polyH, 0, 0 ) );
END;

BEGIN
	tempH := ConvertToPolyline(HDuplicate(objH, 0, 0));
	getProperties_Polyline (tempH, area, perim, xC, yC, Ixx, Iyy, Cxx, Cyy);
	DelObject (tempH);
	area := HArea(objH);
	perim := HPerim(objH);
```
```python
import vs

# ) into a polygon or polyline.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.ConvertToPolyline(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
