# PtInPoly

## Description
Function PtInPoly returns TRUE if the point specified point lies within, or on, the referenced polygon or polyline object.

```pascal
FUNCTION PtInPoly(
				pX,pY : REAL;
				h     : HANDLE): BOOLEAN;
```

```python
def vs.PtInPoly(p, h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|X-Y coordinate point.|
|h|HANDLE|Handle to polygon.|

## Remarks
([[User:CBM-c-_| _c_]] 2021.12.27): This only works on polygons or segments of polylines whose vertex type is corner. Any point on poly segments with other vertex type (bezier, arc, radius, cubic) will return false. Also small polygon sides will cause failure. All in all it is barely usable for anything than large polygons (not polylines) with large sides.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
polyHandle :HANDLE;
locusHandle :HANDLE;
x, y :REAL;
BEGIN
CallTool(-204); polyHandle := FSActLayer;
CallTool(-221); locusHandle := FSActLayer;
GetLocPt(locusHandle, x, y);
Message(PtInPoly(x, y, polyHandle));
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
