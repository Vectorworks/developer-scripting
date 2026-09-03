# MakePolyline

## Description
Creates a polyline using inSourceObject. inSourceObject is unchanged.

```pascal
FUNCTION MakePolyline(inSourceObject : HANDLE): HANDLE;
```

```python
def vs.MakePolyline(inSourceObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSourceObject|HANDLE|The 2D object from which to make a polyline.|

## Remarks
Creates a polyline from inSourceObject. inSourceObject is unchanged.

This routine does not delete inSourceObject; also it creates its returned object not as the last object in the active layer, but immediately after inSourceObject in the stacking order, so if you delete inSourceObject, you will have "replaced" it.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h,h2:HANDLE;
BEGIN
h:=FSActLayer;
h2 := MakePolyline(h);
DelObject(h);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
IF GetRField( objH, 'Flowchart Node', 'Config' ) <> localizedSortStr THEN
	MakePoly := MakePolyline( FInGroup( objH ) )
ELSE
BEGIN
	{ If Config is 'Sort' insert the intersecting point of the two additional lines
	  in the object as otherwise the lines will not be part of the polyline. }
	tempH := MakePolyline( FInGroup( objH ) );
	GetSegPt2( NextObj( tempH ), tempPt.x, tempPt.y );
	InsertVertex( tempH, tempPt.x, tempPt.y, 4, 0 , 0 );
	SetPolyClosed( tempH, TRUE );
	MakePoly := tempH;

tempH 		:= LNewObj;
polylineH 	:= MakePolyline( tempH );
DelObject( tempH );
DelVertex( polylineH, GetVertNum( polylineH ) );

	Get3DInfo(temp_h, garbage_r, garbage_r, JoistHeight);
	Get3DCntr(temp_h, x1, y1, elevationJoists);
	elevationJoists := elevationJoists + ( JoistHeight / 2 );
{					poly_h := MakePolygon(FIn3D(temp_h));}
	poly_h := MakePolyline(FIn3D(temp_h));
	boo := SetParent(poly_h, GetLayer(temp_h));
	HCenter(poly_h, x2, y2);
	HMove(poly_h, x1 - x2, y1 - y2);
	outer_h := poly_h;
```
```python
result = vs.MakePolyline(inSourceObject)
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
