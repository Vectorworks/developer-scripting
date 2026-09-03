# vstGetPt2D

## Description
Returns the point clicked by the user. inPtIndex is 0-based. If you pass in an index that is greater than the number of points clicked by the user, result will be false.

```pascal
PROCEDURE vstGetPt2D(
				inPtIndex : LONGINT;
				VAR outX  : REAL;
				VAR outY  : REAL;
				result    : BOOLEAN);
```

```python
def vs.vstGetPt2D(inPtIndex, result):
    return (outX, outY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPtIndex|LONGINT|   |
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|result|BOOLEAN|   |

## Remarks
Note that [vstNumPts](vstNumPts.md) will return the number of clicked points (a 1-based index). vstGetPt2D is zero-based. So if you're collecting points in the kToolEventPointAdded event you'll likely have to do something like

```pascal
 vstNumPoints(pointNum);
 vstGetPt2D(pointNum-1, ...);
```

[MaKro 6/2018]: ... with pyhton consider using VS:vstGetCurrPt2D ...

## Examples
```pascal
{oval}
1: BEGIN
	vstGetPt2D (0, x1, y1, result);
	vstGetPt2D (1, x2, y2, result);
	IF (x1 <> x2) & (y1 <> y2) THEN
	BEGIN
		{

CASE modeValue_1 OF
	{oval}
	1: BEGIN
		vstGetPt2D (0, x1, y1, result);
		vstGetPt2D (1, x2, y2, result);
		IF (x1 <> x2) & (y1 <> y2) THEN
		BEGIN
			IF (Abs (x2 - x1) > kRMax) & (Abs (y2 - y1) > kRMax) THEN

BEGIN
	vstNameUndoEvent( 'Create Object' );
	vstGetPt2D( 0, pt1.x, pt1.y, result );
	vstGetPt2D( 1, pt2.x, pt2.y, result );
	rot := Vec2Ang( pt2 - pt1 );
	objHand := CreateCustomObjectN( 'Symmetry Label Object', pt1.x, pt1.y, rot, FALSE );
	SetRField( objHand, 'Symmetry Label Object', 'LineLength', Concat( Distance( pt1.x, pt1.y, pt2.x, pt2.y ) ) );
```
```python
import vs

# Returns the point clicked by the user.
inPtIndex = 1
result = True

outX, outY = vs.vstGetPt2D(inPtIndex, result)
vs.Message('vstGetPt2D returned: ' + str((outX, outY)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
