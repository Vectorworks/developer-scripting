# Arc

## Description
Procedure Arc creates an arc object, or a polyline object, in the active document. If p1 and p2 define a perfect square, an arc will be created, with its center point at the center of the square. If p1 and p2 define a rectangle, a polyline will be created which will represent the oval segment defined by the rectangle.

```pascal
PROCEDURE Arc(
				p1X,p1Y    : REAL;
				p2X,p2Y    : REAL;
				StartAngle : REAL;
				ArcAngle   : REAL);
```

```python
def vs.Arc(p1, p2, StartAngle, ArcAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Top left coordinate of bounding box of oval defining the arc.|
|p2|REAL|Bottom right coordinate of bounding box of oval defining the arc.|
|StartAngle|REAL|Start angle of drawn arc.|
|ArcAngle|REAL|Sweep angle of drawn arc.|

## Remarks
The bounding box of the arc or polyline is not the same as the bounding box returned by GetBBox -- unless the sweep angle of the arc is 360 degrees.

## Examples
==== VectorScript ====
```pascal
Arc(0,0,2,2,#45,#90);
{draws an 90 degree arc with a start angle of 45 degrees}
```
==== Python ====
```python
vs.Arc(0,0,2,2,45,90)
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
