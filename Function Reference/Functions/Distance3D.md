# Distance3D

## Description
Returns the 3D distance between two points. Same as Norm.

```pascal
FUNCTION Distance3D(
				x1 : REAL;
				y1 : REAL;
				z1 : REAL;
				x2 : REAL;
				y2 : REAL;
				z2 : REAL): REAL;
```

```python
def vs.Distance3D(x1, y1, z1, x2, y2, z2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x1|REAL|   |
|y1|REAL|   |
|z1|REAL|   |
|x2|REAL|   |
|y2|REAL|   |
|z2|REAL|   |

## Examples
```pascal
	SldrDisp_CamDist := Distance3D	(
									TempCameraPt3D.x, TempCameraPt3D.y, TempCameraPt3D.z,
									TempRefPt3D.x, TempRefPt3D.y, TempRefPt3D.z
									);
END

BEGIN
	currDist := Distance3D( prevPt.x, prevPt.y, prevPt.z, currPt.x, currPt.y, currPt.z );
	lenght	:= lenght + currDist;
END;

		VertBtmRefZ := VertBtmRefZ + VertZInc;
	END;
BeginGroup;
	hAddRailPath := CreateNurbsCurve(AdRailX1,AdRailY1,AdRailZ1,FALSE,1);
	AddVertex3D(hAddRailPath,AdRailX2,AdRailY1+Distance3d(AdRailX1,AdRailY1,AdRailZ1,AdRailX2,AdRailY2,AdRailZ2),AdRailZ1);
```
```python
import vs

# Returns the 3D distance between two points.
x1 = 0.0
y1 = 0.0
z1 = 0.0
x2 = 2.0
y2 = 1.0
z2 = 0.0

distance = vs.Distance3D(x1, y1, z1, x2, y2, z2)
vs.Message('Distance3D returned: ' + str(distance))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
