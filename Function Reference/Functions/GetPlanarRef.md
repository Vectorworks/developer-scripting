# GetPlanarRef

## Description
Get the plane ref ID of the specified object.

```pascal
FUNCTION GetPlanarRef(h : HANDLE): LONGINT;
```

```python
def vs.GetPlanarRef(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object.|

## Examples
```pascal
	gClassN := getClass( gLine );
	SetClass( gParmH, gClassN );
	{ When creating the object, SetClass regenerates it in Screen Plane.
		TO fix this we will SET it in the same plane with the gLine }
	planarRef := GetPlanarRef( gLine );
	SetPlanarRef( gParmH, planarRef );
END

BEGIN
	planarRef := GetPlanarRef(h);
	bIsArcClosed := FALSE;

gRedlinePathObjHan := CreateCustomObjectN(kRedlinePathObjName,HCenX, HCenY,0,FALSE);
planarRef := GetPlanarRef(gUserPathHan);
```
```python
planarRef = vs.GetPlanarRef( hDuplicated )
vs.SetPlanarRef( hDuplicated, 0 )
vs.HScale2D( hDuplicated, 0, 0, dMarkerScale, dMarkerScale, True)
vs.SetPlanarRef( hDuplicated, planarRef )
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
