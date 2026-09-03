# IsCurtainWall

## Description
Use to check whether wall is being used as a curtain wall.

```pascal
FUNCTION IsCurtainWall(hWall : HANDLE): BOOLEAN;
```

```python
def vs.IsCurtainWall(hWall):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWall|HANDLE|Handle to a wall object to check for curtain wall status|

## Examples
```pascal
BEGIN
UID := CreateUUID;
propertyValue := '';
IF IsCurtainWall(WallHand) THEN
BEGIN
	IF GetWallStyle(WallHand) <> '' THEN
		success := IFC_GetPsetProp(GetObject(GetWallStyle(WallHand)), 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType)
	ELSE
		success := IFC_GetPsetProp(WallHand, 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType);
END

IF IsCurtainWall(WallHand) THEN
BEGIN
	IF GetWallStyle(WallHand) <> '' THEN
		success := IFC_GetPsetProp(GetObject(GetWallStyle(WallHand)), 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType)
	ELSE
		success := IFC_GetPsetProp(WallHand, 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType);
END
```
```python
import vs

# Use to check whether wall is being used as a curtain wall.
hWall = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsCurtainWall(hWall)
if ok:
    vs.Message('IsCurtainWall succeeded')
else:
    vs.Message('IsCurtainWall failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
