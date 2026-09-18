# DTM6_GetZatXY

## Description
Calculates the elevation of the specified 2D point on the specified Site Model object.

```pascal
FUNCTION DTM6_GetZatXY(
				hDTMObject : HANDLE;
				TINType    : INTEGER;
				x          : REAL;
				y          : REAL;
				VAR outZ   : REAL):BOOLEAN;
```

```python
def vs.DTM6_GetZatXY(hDTMObject, TINType, x, y):
    return (BOOLEAN, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|A handle to a Site Model object.|
|TINType|INTEGER|A number identifying the Site Model surface (existing or proposed) which elevation is to be calculated.|
|x|REAL|coordinate of the 2D point which elevation is to be calculated.|
|y|REAL|coordinate of the 2D point which elevation is to be calculated.|
|outZ|REAL|Output parameter. The calculated elevation.|

## Remarks
The values of TINType are one of:
*0 - existing - calculates the Z elevation of the point on the existing surface
*1 - proposed - calculates the Z elevation of the point on the proposed surface
*2 - current - depends on the 2D and 3D display parameter of the Site Model. If either of them is proposed then this mode works as '1' otherwise it works as '0'
:The logic is:
::IF (2DDisplay == Proposed) OR (2DDisplay == ExistingOrPoposed) OR (3DDisplay == Proposed) THEN GetZ from [Proposed Surface]
::ELSE GetZ from [Existing Surface]

## Examples
[DTM6_Sample](examples/DTM6_Sample.md)

```pascal
BEGIN
	inBounds         := FALSE;
	IF hDTMObject <> NIL THEN BEGIN
		tmpPt        := ObjectToWorldCoords( objHand, pt );    { convert to world coordinates. }
		IF DTM6_GetZatXY( hDTMObject, whichDTM, tmpPt.x, tmpPt.y, tmpPt.z ) THEN BEGIN
			pt       := WorldToObjectCoords( objHand, tmpPt ); { convert back to object coordinates. }
			pt.z     := pt.z - layerBaseElev;
			inBounds := TRUE;
		END;

BEGIN
BSB := DTM6_GetZatXY( hSelectedDTM, 0 {Existring}, x2, y2, MarkerLoc[PointCount].ExistZ );
END;

{ get the Z elevation at point on the existing Site model. BS, 7/28/2011. }
temp_b := DTM6_GetZatXY( hDTMObject, 0 {existing}, drill_v.x, drill_v.y, z_drill );
```
```python
import vs

# Calculates the elevation of the specified 2D point on the specified Site
# Model object.
hDTMObject = vs.FSActLayer()  # handle to the first selected object on the active layer
TINType = 0
x = 0.0
y = 0.0

ok, outZ = vs.DTM6_GetZatXY(hDTMObject, TINType, x, y)
vs.Message('DTM6_GetZatXY returned: ' + str((ok, outZ)))
```

## See Also
[DTM6_GetDTMObject](DTM6_GetDTMObject.md) | [DTM6_IsDTM6Object](DTM6_IsDTM6Object.md) | [DTM6_IsObjectReady](DTM6_IsObjectReady.md) | [DTM6_IsTypeVisible](DTM6_IsTypeVisible.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
