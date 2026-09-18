# vstNumPts

## Description
Returns the number of points collected by mouse clicks.

```pascal
PROCEDURE vstNumPts(VAR outNumPts : LONGINT);
```

```python
def vs.vstNumPts():
    return outNumPts
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outNumPts|LONGINT|Output parameter.|

## Examples
```pascal
106: BEGIN
	vstNumPts(numPts);
	IF (numPts = 0) THEN vstEnableMode(1, TRUE);
END;

BEGIN
	vstNumPts( numPts );
	IF numPts = 1 THEN DSelectAll;
END;

DSelectAll;
vstNumPts(ptCnt);
if ptCnt > 2 then BEGIN
	ALLOCATE pts [1..ptCnt];
	for cnt := 1 to ptCnt DO vstGetPt3D(cnt - 1, pts[cnt].x, pts[cnt].y, z, result);
	planRot := GetPrefReal(93);
```
```python
import vs

# Returns the number of points collected by mouse clicks.
result = vs.vstNumPts()
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
