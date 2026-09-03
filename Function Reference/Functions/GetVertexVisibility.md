# GetVertexVisibility

## Description
Returns the visibility of the specified vertex of the referenced object.

```pascal
FUNCTION GetVertexVisibility(
				h       : HANDLE;
				vertnum : INTEGER): BOOLEAN;
```

```python
def vs.GetVertexVisibility(h, vertnum):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the polygon or polyline|
|vertnum|INTEGER|Index of the vertex (zero-based).|

## Examples
```pascal
		THEN closeShape := TRUE {so it will default to true the first time}
		ELSE closeShape := Str2Boo(GetElement(xmlID, 'PropertyLine/closeShape'));
	xmlID := ReleaseXML(xmlID);
end else BEGIN
	closeShape := GetVertexVisibility(pathHandle, GetVertNum(pathHandle) - 1);
	GetSymLoc(objHand, originPt.x, originPt.y);
	objectRotation := GetSymRot(objHand);
	Polyline2ARRAY(pathHandle, 179, .1", FALSE, FALSE, verts, vertCnt);
	ALLOCATE segs [1..vertCnt];

yAxis.x := 0;
yAxis.y := 1;
origin.x := 0;
origin.y := 0;
for cnt := 1 to vertex_cnt - 1 do if GetVertexVisibility(pathHandle, cnt - 1) then BEGIN
	pt1.x := vertices[cnt,1];
	pt1.y := vertices[cnt,2];
	pt2.x := vertices[cnt+1,1];
	pt2.y := vertices[cnt+1,2];
	if vertices[cnt,3] = 0 then BEGIN

BEGIN
	GetPolylineVertex(hOrigRefPathObj,i,CurrentVertX,CurrentVertY,CurrentPolyVertType,PolyVertRadius);
	SetPolylineVertex (hCenterLine,i,CurrentVertX,CurrentVertY,CurrentPolyVertType,PolyVertRadius,TRUE);
	VertVis := GetVertexVisibility (hOrigRefPathObj,i);
	SetVertexVisibility (hCenterLine,i,VertVis);
END;
```
```python
import vs

# Returns the visibility of the specified vertex of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
vertnum = 1

ok = vs.GetVertexVisibility(h, vertnum)
if ok:
    vs.Message('GetVertexVisibility succeeded')
else:
    vs.Message('GetVertexVisibility failed')
```

## See Also
VS Functions:
[SetVertexVisibility](SetVertexVisibility.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
