# CreateLoftSurfaces

## Description
Creates NURBS surfaces by interpolating a group of cross-section curves.  The nurbs curves are lofted in the order in which they were added to the group.

```pascal
FUNCTION CreateLoftSurfaces(
				groupCurvesHd : HANDLE;
				bRule         : BOOLEAN;
				bClose        : BOOLEAN;
				bSolid        : BOOLEAN): HANDLE;
```

```python
def vs.CreateLoftSurfaces(groupCurvesHd, bRule, bClose, bSolid):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|groupCurvesHd|HANDLE|   |
|bRule|BOOLEAN|   |
|bClose|BOOLEAN|   |
|bSolid|BOOLEAN|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
	h, grH : HANDLE;
	x, y, z, offset : REAL;
	bRule, bClose, bSolid : BOOLEAN;
	
BEGIN
	x := 10m;
	y := 20m;
	z := 3m;
	offset := 5m;
	
	BeginGroupN(grH);
		h := CreateNurbsCurve(-x/2, 0, 0, true, 1);
		AddVertex3D(h, -x/2, y, 0);
		AddVertex3D(h, x/2, y, 0);
		AddVertex3D(h, x/2, 0, 0);

		h := CreateNurbsCurve(-x/2 -offset, 0, z, true, 1);
		AddVertex3D(h, -x/2 -offset, y +offset, z);
		AddVertex3D(h, x/2 +offset, y +offset, z);
		AddVertex3D(h, x/2 +offset, 0, z);
	EndGroup;
	
	bRule := TRUE;
	bClose := FALSE;
	bSolid := FALSE;
	
	grH := CreateLoftSurfaces(grH, bRule, bClose, bSolid);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	x = 10
	y = 20
	z = 3
	offset = 5

	grH = vs.BeginGroupN(None)
	
	h = vs.CreateNurbsCurve(-x/2, 0, 0, True, 1)
	vs.AddVertex3D(h, -x/2,y,0)
	vs.AddVertex3D(h, x/2,y,0)
	vs.AddVertex3D(h, x/2,0,0)

	h = vs.CreateNurbsCurve(-x/2-offset,0,z, True, 1)
	vs.AddVertex3D(h, -x/2-offset, y+offset, z)
	vs.AddVertex3D(h, x/2+offset, y+offset, z);
	vs.AddVertex3D(h, x/2+offset, 0, z);

	vs.EndGroup()
	
	bRule = True
	bClose = False
	bSolid = False
	
	grH = vs.CreateLoftSurfaces(grH, bRule, bClose, bSolid)
	
Example()
```

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
