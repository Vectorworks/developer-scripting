# DelVertex

## Description
Procedure DelVertex deletes a vertex from the referenced object. Parameter vertexNum specifies the vertex to be deleted.

```pascal
PROCEDURE DelVertex(
				objectHd  : HANDLE;
				vertexNum : INTEGER);
```

```python
def vs.DelVertex(objectHd, vertexNum):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to polygon.|
|vertexNum|INTEGER|Index of vertex to be deleted.|

## Examples
```pascal
h1 := OffsetPolygon(walls[cnt1], -1");
for cnt2 := GetVertNum(h1) downto 2 do BEGIN
	GetPolyPt(h1, cnt2 - 1, pt1.x, pt1.y);
	GetPolyPt(h1, cnt2,     pt2.x, pt2.y);
	IF Abs(Norm(pt2 - pt1)) < .0625" THEN DelVertex(h1, cnt2);
END;

tempH 		:= LNewObj;
polylineH 	:= MakePolyline( tempH );
DelObject( tempH );
DelVertex( polylineH, GetVertNum( polylineH ) );

	Add2DVertex(x, y, t, r);
END;
EndPoly;
poly := LNewObj;
IF GetVertNum(h) = 2 THEN DelVertex(poly, 2);
IF copyHoles THEN
	BEGIN
	boo := GetNumHoles(h, holeCnt);
	FOR cnt := 1 TO holeCnt DO
```
```python
import vs

# Procedure DelVertex deletes a vertex from the referenced object.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
vertexNum = 1

vs.DelVertex(objectHd, vertexNum)
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
