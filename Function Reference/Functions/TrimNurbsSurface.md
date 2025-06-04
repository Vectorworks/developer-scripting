# TrimNurbsSurface

## Description
Trims the NURBS surface by a given NURBS curve.

```pascal
FUNCTION TrimNurbsSurface(
				surfaceHandle : HANDLE;
				curveHandle   : HANDLE): BOOLEAN;
```

```python
def vs.TrimNurbsSurface(surfaceHandle, curveHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|surfaceHandle|HANDLE|Handle to a NURBS surface to trim.|
|curveHandle|HANDLE|Handle to a NURBS curve for trimming.|

## Remarks
It returns true if the curve is attached to the surface as trimmed curve.

## Examples
```pascal
PROCEDURE Example;
VAR
	surfaceH, curveH :HANDLE;
	bFlag :BOOLEAN;

BEGIN
	surfaceH:= CreateNurbsSurface(3, 3, 1, 1);
	NurbsSetPt3D(surfaceH, 0, 0, 0, 0, 0);
	NurbsSetPt3D(surfaceH, 0, 1, 1, 0, 0);
	NurbsSetPt3D(surfaceH, 0, 2, 2, 0, 0);
	NurbsSetPt3D(surfaceH, 1, 0, 0, 1, 0);
	NurbsSetPt3D(surfaceH, 1, 1, 1, 1, 1);
	NurbsSetPt3D(surfaceH, 1, 2, 2, 1, 0);
	NurbsSetPt3D(surfaceH, 2, 0, 0, 2, 0);
	NurbsSetPt3D(surfaceH, 2, 1, 1, 2, 0);
	NurbsSetPt3D(surfaceH, 2, 2, 2, 2, 0);

	curveH := CreateNurbsCurve(0, 0, 0, TRUE, 2);
	AddVertex3D(curveH, 1, 1, 0);
	AddVertex3D(curveH, 2, 0, 0);

	bFlag := TrimNurbsSurface(surfaceH, curveH);
END;
RUN(Example);
```

## See Also
VS Functions:
[CreateNurbsSurface](CreateNurbsSurface.md) 
| [CreateNurbsCurve](CreateNurbsCurve.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
