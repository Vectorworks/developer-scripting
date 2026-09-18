# MakePolygon

## Description
MakePolygon creates a 2D Polygon using inSourceObject. Does not delete inSourceObject.

```pascal
FUNCTION MakePolygon(inSourceObject : HANDLE): HANDLE;
```

```python
def vs.MakePolygon(inSourceObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSourceObject|HANDLE|inSource object should be a 2D object that can be polygonalized.|

## Remarks
This routine creates its returned object not as the last object in the active layer, but immediately after inSourceObject in the stacking order, so if you delete inSourceObject, you will have "replaced" it.

See also: [ConvertToPolygon](ConvertToPolygon.md)

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
CallTool(-204);
h := FSActLayer;
h := MakePolygon(h);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
	h1 := HDuplicate(FIn3D(h), 0, 0);
	ok := TRUE;
END;
if ok then BEGIN
	h2 := MakePolygon(h1);
	DelObj(h1);
	wall_cnt := wall_cnt + 1;
	walls[wall_cnt] := OffsetPolygon(h2, 1");
	DelObj(h2);

BEGIN
	polygon := MakePolygon(h);
	numPolyVerts := GetVertNum (polygon);
	ALLOCATE polyPt [1..numPolyVerts];
	ALLOCATE midPt [1..numPolyVerts];
	For I := 1 to numPolyVerts DO

IF GetType (objH) <> 5 THEN
	tempH := MakePolygon (objH)
ELSE tempH := objH;
```
```python
result = vs.MakePolygon(inSourceObject)
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
