# GetVPCropObject

## Description
Gets the specified viewport's crop object, if any.

```pascal
FUNCTION GetVPCropObject(viewportHandle : HANDLE): HANDLE;
```

```python
def vs.GetVPCropObject(viewportHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |

## Examples
```pascal
BEGIN
	pioParentVPCropHand	:= GetVPCropObject( pioParentVPHand );
	pioLayScale := GetObjectVariableReal( pioParentVPHand, 1003 );
	SheetLayerDPI := GetObjectVariableInt( GetLayer( pioParentVPHand ), 155 );
	pioParentVPLocPt.x := GetObjectVariableReal( pioParentVPHand, 1024 );
	pioParentVPLocPt.y := GetObjectVariableReal( pioParentVPHand, 1025 );

		-VPShiftOffsetPt.x,
		-VPShiftOffsetPt.y
		);
{ move vp crop }
IF ( GetVPCropObject( pioParentVPHand ) <> NIL ) THEN
BEGIN
	HCenter( GetVPCropObject( pioParentVPHand ), VPCropCenterPt.x, VPCropCenterPt.y );
	HMove	(
			GetVPCropObject( pioParentVPHand ),
			-VPShiftOffsetPt.x,
			-VPShiftOffsetPt.y
```
```python
import vs

# Gets the specified viewport's crop object, if any.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetVPCropObject(viewportHandle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
