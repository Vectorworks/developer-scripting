# SetCustomObjectProfileGroup

## Description
Sets the profile group for a path custom object.

```pascal
FUNCTION SetCustomObjectProfileGroup(
				objectHand       : HANDLE;
				profileGroupHand : HANDLE): BOOLEAN;
```

```python
def vs.SetCustomObjectProfileGroup(objectHand, profileGroupHand):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|
|profileGroupHand|HANDLE|Handle to profile group.|

## Examples
```pascal
		SetRField(loch, kHidRecName, kNoteUUID, '');
	END;
EndGroup;
loch := LNewObj;
boo := SetCustomObjectProfileGroup(gnH, loch);

EndGroup;
h := LNewObj;
SetClass(h,noneClass);
bsb := SetCustomObjectProfileGroup(pluginH, h);
{Delete the symbol if I imported it}
IF ImportedMarker1 THEN
	BEGIN
	TempHand := GetObject(actualMarker1Name);

BEGIN
gTempH := HDuplicate(gRoofH,0,0);
temp_b := SetCustomObjectProfileGroup(gMyHand,gTempH);
END;
```
```python
bResult = vs.SetCustomObjectProfileGroup( gObjHandle, vs.LNewObj() )
```

## See Also
VS Functions:
[GetCustomObjectProfileGroup](GetCustomObjectProfileGroup.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
