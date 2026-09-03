# DTM6_IsTypeVisible

## Description
Check if the specified TIN type of the specified Site Model object is visible.

```pascal
FUNCTION DTM6_IsTypeVisible(
				hDTMObject : HANDLE;
				TINType    : INTEGER):BOOLEAN;
```

```python
def vs.DTM6_IsTypeVisible(hDTMObject, TINType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDTMObject|HANDLE|A handle to the Site Model object.|
|TINType|INTEGER|A number specifying which TIN type is to be check for visibility. See the remarks for detail information of the options.|

## Remarks
Here is the list of TINType values. The function will return TRUE when these conditions are met. 2DDisplay and 3DDisplay are parameters of the Site Model object controlling if the Existing or Proposed model are to be displayed in 2D or 3D:
*0 - 2D/3D existing  -- IF (2DDisplay == Existing) OR (2DDisplay == ExistingOrProposed) OR (3DDisplay == Existing) THEN RETURN TRUE
*1 - 2D/3D proposed -- IF (2DDisplay == Proposed) OR (2DDisplay == ExistingOrProposed) OR (3DDisplay == Proposed) THEN RETURN TRUE
*2 - 2D existing -- IF (2DDisplay == Existing) OR (2DDisplay == ExistingOrProposed) THEN RETURN TRUE
*3 - 2D proposed -- IF (2DDisplay == Proposed) OR (2DDisplay == ExistingOrProposed) THEN RETURN TRUE
*4 - 3D existing -- IF (3DDisplay == Existing) THEN RETURN TRUE
*5 - 3D proposed -- IF (3DDisplay == Proposed)  THEN RETURN TRUE

## Examples
[DTM6_Sample](examples/DTM6_Sample.md)

```pascal
checkBox8 := gDrawExisting;
SetBooleanItem(dialog1,  8,gDrawExisting);	{Draw Existing Site Profile}
checkBox10 := gDrawProposed;
SetBooleanItem(dialog1, 10,gDrawProposed);	{Draw Proposed Site Profile}
IF NOT DTM6_IsTypeVisible( hSelectedDTM, 1 {Proposed} ) THEN
	BEGIN
	EnableItem(dialog1, 10,FALSE);
	EnableItem(dialog1, 11,FALSE);
	gDrawProposed := FALSE;
	SetBooleanItem(dialog1, 10,gDrawProposed);
	END;

BEGIN
IF (pMode = 1) THEN SetBooleanItem(dialog1,  5, TRUE) ELSE SetBooleanItem(dialog1,  6, TRUE);
IF (NOT DTM6_IsTypeVisible( hDTMObject, 0 {existring} )) AND (NOT DTM6_IsTypeVisible( hDTMObject, 1 {proposed} )) THEN
	BEGIN
	SetBooleanItem(dialog1, 5,TRUE);
	EnableItem(dialog1, 6,FALSE);
	END;

{we are interested in 3D since currently this command switches to 3D}
haveExist	:= DTM6_IsTypeVisible( hDTMObject, 4 {3D Existring} );
haveProp	:= DTM6_IsTypeVisible( hDTMObject, 5 {3D Proposed} );
{ check to see if we should disable the propsed analysis button }
if not haveExist then BEGIN
	SetBooleanItem(dlogID,  6, TRUE );
```
```python
import vs

# Check if the specified TIN type of the specified Site Model object is visible.
hDTMObject = vs.FSActLayer()  # handle to the first selected object on the active layer
TINType = 0

ok = vs.DTM6_IsTypeVisible(hDTMObject, TINType)
if ok:
    vs.Message('DTM6_IsTypeVisible succeeded')
else:
    vs.Message('DTM6_IsTypeVisible failed')
```

## See Also
[DTM6_GetDTMObject](DTM6_GetDTMObject.md) | [DTM6_IsDTM6Object](DTM6_IsDTM6Object.md) | [DTM6_IsObjectReady](DTM6_IsObjectReady.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
