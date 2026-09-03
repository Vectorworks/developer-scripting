# GetWallStyle

## Description
Gets the name of the Wall Style for theWall.

```pascal
FUNCTION GetWallStyle(theWall : HANDLE): STRING;
```

```python
def vs.GetWallStyle(theWall):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|

## Remarks
Gets the name of the Wall Style for theWall

## Examples
```pascal
BEGIN
	IF GetWallStyle(WallHand) <> '' THEN
		success := IFC_GetPsetProp(GetObject(GetWallStyle(WallHand)), 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType)
	ELSE
		success := IFC_GetPsetProp(WallHand, 'Pset_CurtainWallCommon', 'Reference', propertyValue, propertyType);
END

if walls[cnt].tipe = 0 then BEGIN
	if oldWallCnt > 0 then BEGIN
		{Find the first matching wall, then short-circuit.}
		for cnt3 := 1 to oldWallCnt do BEGIN
			IF (oldWalls[cnt3].tipe = 0) & (GetWallStyle(oldWalls[cnt3].h) = style) then BEGIN
				near_dist := WallComparisonStraight(cnt, cnt3);
				found := cnt3;
				cnt3 := oldWallCnt;
			END;

BEGIN
	wallStyleName := GetWallStyle(wall_h);
	wallStyleHand := GetObject(wallStyleName);
	IF wallStyleHand <> NIL THEN BEGIN
		result := GetNumberOfComponents( wallStyleHand, numberOfComponents );
		temp_r := 0;
```
```python
import vs

# Gets the name of the Wall Style for theWall.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetWallStyle(theWall)
vs.Message('GetWallStyle returned: ' + str(text))
```

## See Also
VS Functions:
[SetWallStyle](SetWallStyle.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
