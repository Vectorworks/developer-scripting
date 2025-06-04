# DTM6_SendToSurface

## Description
Send the specified object to the surface of the SiteModel specified.

NOTE! The 3D polygons receive new points where it crosses the SiteModel.

```pascal
FUNCTION DTM6_SendToSurface(
				hDTMObject : HANDLE;
				hObject    : HANDLE;
				TINType    : INTEGER):BOOLEAN;
```

```python
def vs.DTM6_SendToSurface(hDTMObject, hObject, TINType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|A handle of the Site Model object to be used.|
|hObject|HANDLE|A handle of the object to be send to surface.|
|TINType|INTEGER|A number identifying the Site Model surface (existing or proposed) which elevation is to be calculated.|

## Remarks
The values of TINType are one of:
*0 - existing - calculates the Z elevation of the point on the existing surface
*1 - proposed - calculates the Z elevation of the point on the proposed surface
*2 - current - depends on the 2D and 3D display parameter of the Site Model. If either of them is proposed then this mode works as '1' otherwise it works as '0'
:The logic is:
::IF (2DDisplay == Proposed) OR (2DDisplay == ExistingOrPoposed) OR (3DDisplay == Proposed) THEN GetZ from [Proposed Surface]
::ELSE GetZ from [Existing Surface]
[[User:Ptr|Ptr]] [2020.09.14]:When applying this call on a 2D object, that 2D object gets converted into a 3D polygon. The handle to the 2D object will not be linked to this 3D polygon. "vs.LNewObj()" will not return the handle to the 3D polygon.

## Examples
==== Python ====
```python
_, _sPIOName, _hPIO, _hPIORecord, _hWall = vs.GetCustomObjectInfo()  # Get info from current PIO instance
_hPath = vs.GetCustomObjectPath(_hPIO)
_hDTM = vs.DTM6_GetDTMObject(vs.GetLayer(_hPIO), False)  # Get Site Model on the PIO's layer
_hPoly2D = vs.HDuplicate(_hPath, 0, 0)
_b = vs.DTM6_SendToSurface(_hDTM, _hPoly2D, 0)
vs.Locus(0, 0)  # Create a dummy object
_h = vs.LNewObj()
_hPoly3D = vs.PrevObj(_h)
vs.DelObject(_h)  # Delete the dummy object
```

## See Also
[DTM6_GetDTMObject](DTM6_GetDTMObject.md) | [DTM6_IsDTM6Object](DTM6_IsDTM6Object.md) | [DTM6_IsObjectReady](DTM6_IsObjectReady.md) | [DTM6_IsTypeVisible](DTM6_IsTypeVisible.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
