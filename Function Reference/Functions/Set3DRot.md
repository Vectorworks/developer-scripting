# Set3DRot

## Description
Procedure Set3DRot rotates the referenced 3D object about a specified 3D point.  It works with the following 3D objects: extrude, multiple extrude, sweep, mesh, 3D polygon, solid, CSG solid, group, symbol, plug-in object, NURBS curve, NURBS surface.

[[Image:3drotate.gif]]

The difference between Set3DRot and [[VS:SetRot3D| SetRot3D]] is that Set3DRot adds the specified rotation to the existing rotation of the object, whereas [[VS:SetRot3D| SetRot3D]] does not consider the existing rotation, and merely makes the object rotation match the specified values.

```pascal
PROCEDURE Set3DRot(
				h         : HANDLE;
				xAngle    : REAL;
				yAngle    : REAL;
				zAngle    : REAL;
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.Set3DRot(h, xAngle, yAngle, zAngle, xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D object.|
|xAngle|REAL|X axis rotation angle.|
|yAngle|REAL|Y axis rotation angle.|
|zAngle|REAL|Z axis rotation angle.|
|xDistance|REAL|X coordinate of center of rotation.|
|yDistance|REAL|Y coordinate of center of rotation.|
|zDistance|REAL|Z coordinate of center of rotation.|

## Remarks
(Gerard Jonker, 5 April 2006): The xDistance and yDistance parameters use the Absolute Origin, so you have to correct for a moved User Origin (see example).

## Examples
{{Manipulate3DObjects}}
```pascal
PROCEDURE Example;
BEGIN
    Poly3D(0, -100, -200,  0, 100, -200,  0, 100, 200,  0, -100, 200,  0, -100, -200);
    Set3DRot(LNewObj, 45, 45, 45,  0, 0, 0);
END;
RUN(Example);
```

```pascal
{ Gerard Jonker, 2006 }
PROCEDURE test;	{ make sure Symbol-1 exists before running this script }
VAR	
    xAngle, yAngle, zAngle,
    xDistance, yDistance, zDistance, 
    xOrigin, yOrigin, foney: REAL;
    h	: HANDLE;
    bool	: BOOLEAN;
BEGIN
    GetOrigin(xOrigin, yOrigin); { retrieve user origin }

    Symbol('Symbol-1', 0, 0, 0); { places symbol on user origin }
    h := LNewObj; { get a handle to the symbol }
    GetSymLoc(h, xDistance, yDistance);
    Get3DCntr (h, foney, foney, zDistance); {x,y are unreliable in case of a hybrid symbol }

    xAngle := 10.12345;
    yAngle := 10.12345;
    zAngle := 10.12345;

    Set3Drot(h, xAngle, yAngle, zAngle, xOrigin + xDistance, yOrigin + yDistance, zDistance);
    { you can actually rotate a hybrid symbol using Set3DRot although it is advised not to }
    { the rotation over the x and y axes will be set back to 0 when the symbol is edited }
END;
RUN(test);
==== Python ====
<code lang="py">
```

## See Also
VS Functions:
[SetRot3D](SetRot3D.md)

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
