# ConvertTo3DPolys

## Description
Converts an object to 3D polygons. This function successfully converts rectangles, circles, arcs, polylines, polygons, ovals, lines, straight walls, curved walls, and roofs.

```pascal
FUNCTION ConvertTo3DPolys(original : HANDLE): HANDLE;
```

```python
def vs.ConvertTo3DPolys(original):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|original|HANDLE|Handle to the original object.|

## Remarks
This function is failing within VSOs.



Return Handle is a handle to a group containing the 3D Poly.  The original 2D poly is destroyed by this command, so be warned that original poly handle is most likely garbage after running this function.

The group will contain a single 3D poly if the original source polyline contained no holes. If the source polyline contained holes the group will contain multiple 3D polygons that trace the outline and the holes.

The following object types fail to be converted: Dimensions.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := ConvertTo3DPolys(FSActLayer);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	h = vs.ConvertTo3DPolys(vs.FSActLayer())
Example()
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
