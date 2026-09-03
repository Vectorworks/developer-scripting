# GetVPGroup

## Description
Gets the specified viewport group.

groupType values:
Crop = 1
Annotation = 2
Cache = 3

```pascal
FUNCTION GetVPGroup(
				viewportHandle : HANDLE;
				groupType      : INTEGER): HANDLE;
```

```python
def vs.GetVPGroup(viewportHandle, groupType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|groupType|INTEGER|   |

## Examples
```pascal
BEGIN
VPGrpHand := GetVPGroup(h,2);
ForEachObjectInList(FindDL,0,2,FInGroup(VPGrpHand));
END

gCurrAnnotationGroupH := NIL;
{search in the annotation group of the Viewport object}
IF ( GetType( Hob ) = 122{Viewport OBJECT!})
THEN BEGIN
	tempH := GetVPGroup( HOb, 2{Annotation group});
	if ( tempH <> nil ) then BEGIN
		gCurrAnnotationGroupH := tempH;
		gStop := FALSE;
		CASE gProcessWhat OF

BEGIN
	gNumSelObjs := 0;
	TmpGroupHan := GetVPGroup (containerHandle,2);
	tempObjH := FINGroup (TmpGroupHan);
	ForEachObjectInList (CaptureSelection2, 2, 0, tempObjH);
END
```
```python
import vs

# Gets the specified viewport group.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
groupType = 0

objHandle = vs.GetVPGroup(viewportHandle, groupType)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
