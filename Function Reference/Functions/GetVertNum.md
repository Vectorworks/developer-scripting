# GetVertNum

## Description
Function GetVertNum returns the number of vertices of the referenced polygon or polyline object.

```pascal
FUNCTION GetVertNum(PolyHd : HANDLE): INTEGER;
```

```python
def vs.GetVertNum(PolyHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PolyHd|HANDLE|Handle to polygon.|

## Examples
```pascal
BEGIN
	GetVertexType := -1;
	numberOfVertices := GetVertNum(lineHandle);

{ortogonality of the segments and if it is an Open polygon}
polygons := polygons + 1;
if polygons > 1 then Set2FALSE
else BEGIN
	if GetVertNum( tempH ) <> 4 then Set2FALSE
		else if ispolyclosed(temph) then BEGIN
			GetPolylineVertex( tempH, 1, vec1[1], vec1[2], verttype, arcrad );
			GetPolylineVertex( tempH, 2, vec2[1], vec2[2], verttype, arcrad );
			GetPolylineVertex( tempH, 3, vec3[1], vec3[2], verttype, arcrad );
			vec1 := vec1 - vec2;
			vec3 := vec3 - vec2;

net_cnt := 0;
for cnt1 := 1 to wall_cnt do BEGIN
	IF doGross THEN BEGIN
		h1 := OffsetPolygon(walls[cnt1], -1");
		for cnt2 := GetVertNum(h1) downto 2 do BEGIN
			GetPolyPt(h1, cnt2 - 1, pt1.x, pt1.y);
			GetPolyPt(h1, cnt2,     pt2.x, pt2.y);
			IF Abs(Norm(pt2 - pt1)) < .0625" THEN DelVertex(h1, cnt2);
		END;
```
```python
import vs

# Function GetVertNum returns the number of vertices of the referenced
# polygon or polyline object.
PolyHd = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetVertNum(PolyHd)
vs.Message('GetVertNum returned: ' + str(count))
```
See also in tutorials: [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md)

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
