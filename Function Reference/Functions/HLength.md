# HLength

## Description
Function HLength returns the length of a line.

```pascal
FUNCTION HLength(h : HANDLE): REAL;
```

```python
def vs.HLength(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
```pascal
BEGIN
IF (IsArcBasedWall(wallHandle)) THEN
	RoundWallRadius := 5729.28 / ((100 * HAngle(wallHandle)) / HLength(wallHandle));
END;

BEGIN
	nurbsHandle := GetCustomObjectPath(objHand);
	nurbsLength := HLength(nurbsHandle);
	gStationSpacing := Str2Num(GetRField(objHand, objName, 'Station Spacing'));
	IF gStationSpacing < 12" THEN gStationSpacing := 12";
	nurbsPtCnt := Trunc(nurbsLength / gStationSpacing) + 2;
	ALLOCATE nurbs [1..nurbsPtCnt];

BEGIN
	h1 := FInGroup(handleToGroup);
	WHILE h1 <> NIL DO BEGIN
		h2 := NextObj(h1);
		IF (GetType(h1) = 2) & (HLength(h1) < fuzz) THEN DelObj(h1);
		h1 := h2;
	END;
```
```python
import vs

# Function HLength returns the length of a line.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

distance = vs.HLength(h)
vs.Message('HLength returned: ' + str(distance))
```
See also in tutorials: [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
