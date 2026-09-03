# SetCustomObjectWallHoleGroup

## Description
Set wall hole geometry for a parametric object.

See [[VS:Parametric Custom Opening in Wall]] for more info.

```pascal
FUNCTION SetCustomObjectWallHoleGroup(
				objectHand : HANDLE;
				holeGroup  : HANDLE): BOOLEAN;
```

```python
def vs.SetCustomObjectWallHoleGroup(objectHand, holeGroup):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to parametric object.|
|holeGroup|HANDLE|Handle to object or group that contains geometry for wall hole.|

## Examples
```pascal
FillPat(1);
BeginXtrd (0,Height);
	RectangleN (LCutX,-25', 90, 0, RCutX-LCutX, 50');
EndXtrd;
GroupWorked := SetCustomObjectWallHoleGroup (ghParm,LNewObj);
PopAttrs;

				OvalN (-Width/2-LeftBord,0, 90, 0, Width+RightBord+LeftBord, Height);
			EndXtrd;
			SET3Drot(LNewObj,90,0,0,0,0,0);
		END;
GroupWorked := SetCustomObjectWallHoleGroup (ghParm,LNewObj);
PopAttrs;
```
```python
import vs

# Set wall hole geometry for a parametric object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer
holeGroup = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetCustomObjectWallHoleGroup(objectHand, holeGroup)
if ok:
    vs.Message('SetCustomObjectWallHoleGroup succeeded')
else:
    vs.Message('SetCustomObjectWallHoleGroup failed')
```

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
