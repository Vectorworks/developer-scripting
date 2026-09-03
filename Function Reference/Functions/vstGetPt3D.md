# vstGetPt3D

## Description
Returns the point picked by the user at the specified index.

```pascal
PROCEDURE vstGetPt3D(
				inPtIndex : LONGINT;
				VAR outX  : REAL;
				VAR outY  : REAL;
				VAR outZ  : REAL;
				result    : BOOLEAN);
```

```python
def vs.vstGetPt3D(inPtIndex, result):
    return (outX, outY, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPtIndex|LONGINT|   |
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|outZ|REAL|Output parameter.|
|result|BOOLEAN|   |

## Examples
```pascal
DSelectAll;
vstNumPts(ptCnt);
if ptCnt > 2 then BEGIN
	ALLOCATE pts [1..ptCnt];
	for cnt := 1 to ptCnt DO vstGetPt3D(cnt - 1, pts[cnt].x, pts[cnt].y, z, result);
	planRot := GetPrefReal(93);
	BeginPoly;
		FOR cnt := 1 TO ptCnt DO AddPoint(pts[cnt].x, pts[cnt].y);
	EndPoly;

begin
	SetCursor (SmCrossC);
	If Is3dView then
		vstGetPt3D(0, x1, y1, z1, result)
	else
		vstGetPt2D(0, x1, y1, result);
end;

BEGIN
	vstGetPt3D (0, x1, y1, z1, result);
	IF gFastenerType = 1 THEN vstGetPt3D (1, x2, y2, z2, result);
END
```
```python
import vs

# Returns the point picked by the user at the specified index.
inPtIndex = 1
result = True

outX, outY, outZ = vs.vstGetPt3D(inPtIndex, result)
vs.Message('vstGetPt3D returned: ' + str((outX, outY, outZ)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
