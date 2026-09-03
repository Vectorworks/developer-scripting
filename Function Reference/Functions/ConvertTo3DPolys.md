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
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := ConvertTo3DPolys(FSActLayer);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	h = vs.ConvertTo3DPolys(vs.FSActLayer())
Example()
```

```pascal
{ConvertTo3DPolys fails if object is not visable}
dpathHandle := HDuplicate(nurbsHandle,0,0);
IF GetCVis(GetClass(dpathHandle)) <> 0 THEN
	SetClass(dpathHandle,noneClass);
pathHandle := ConvertTo3DPolys(dpathHandle);
tempH := FInGroup(pathHandle);
vertCnt := 0;
while tempH <> nil do BEGIN
	tmpVertCnt := GetVertNum(tempH);

BEGIN
	old3DConRes := GetPrefInt(56);
	SetPrefInt(5556, 128);
	group_h := ConvertTo3DPolys(h);
	temp_h := FInGroup(group_h);
	poly_cnt := 0;
	while temp_h <> nil do BEGIN
		poly_cnt := poly_cnt + 1;

tempH2 := copyPoly(pathHand);
{ create a 3D polys based on the path. }
tempH  := ConvertTo3DPolys(tempH2);
```
```python
import vs

# Converts an object to 3D polygons.
original = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.ConvertTo3DPolys(original)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
