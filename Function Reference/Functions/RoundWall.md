# RoundWall

## Description
Procedure RoundWall creates a counter-clockwise round wall.

```pascal
PROCEDURE RoundWall(
				centerPtX,centerPtY : REAL;
				startPtX,startPtY   : REAL;
				endPtX,endPtY       : REAL);
```

```python
def vs.RoundWall(centerPt, startPt, endPt):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|centerPt|REAL|Center point of wall arc.|
|startPt|REAL|Start point of wall arc.|
|endPt|REAL|End point of wall arc.|

## Remarks
Creates a round wall the that is centered on the arc specified by the the three input points.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
x1, y1, x2, y2, x3, y3 :REAL;
lineHandle :HANDLE;
BEGIN
GetPt(x1, y1);
GetPtL(x1, y1, x2, y2);
MoveTo(x1, y1);
LineTo(x2, y2);
lineHandle := LNewObj;
GetPtL(x2, y2, x3, y3);
IF lineHandle &lt;&gt; NIL THEN DelObject(lineHandle);
RoundWall(x1, y1, x2, y2, x3, y3);
END;
RUN(Example);
```
==== Python ====
```python

```

## See Also
VS Functions:
[Wall](Wall.md)

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
