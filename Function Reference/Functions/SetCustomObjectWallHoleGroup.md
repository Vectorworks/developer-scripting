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

## Version
Availability: from Vectorworks14.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
