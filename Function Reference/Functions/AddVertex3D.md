# AddVertex3D

## Description
Procedure AddVertex3D adds a 3D vertex to the referenced 3D polygon object.

```pascal
PROCEDURE AddVertex3D(
				objectHd : HANDLE;
				pX,pY,pZ : REAL);
```

```python
def vs.AddVertex3D(objectHd, p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to object.|
|p|REAL|Location of 3D vertex point.|

## Examples
```pascal
GetPolyPt(h, 1, x, y);
tempObjH := CreateNurbsCurve(x, y, 0, TRUE, 2);
for cnt := 2 to GetVertNum(h) do BEGIN
	GetPolyPt(h, cnt, x, y);
	AddVertex3D(tempObjH, x, y, 0);
END;

	nurbsHandle := CreateNurbsCurve(nurbs[1].x, nurbs[1].y, (nurbs[1].z - zCorrection), byCtrlPts, longDegree);
	for cnt := 2 to nurbsPtCnt DO AddVertex3D(nurbsHandle, nurbs[cnt].x, nurbs[cnt].y, (nurbs[cnt].z - zCorrection) );
	IF (objHand <> NIL) & (nurbsHandle <> NIL) THEN boo := SetCustomObjectPath(objHand, nurbsHandle);
END;

BEGIN
	AddVertex3D(wholeNurbsHand, pt1.x, pt1.y, pt1.z - vertOffset);
	nurbsHand := CreateNURBSCurve(pt1.x, pt1.y, pt1.z - vertOffset, TRUE, 2);
END;
```
```python
import vs

# Procedure AddVertex3D adds a 3D vertex to the referenced 3D polygon object.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
p = (0, 0)

vs.AddVertex3D(objectHd, p)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[Add3DPt](Add3DPt.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
