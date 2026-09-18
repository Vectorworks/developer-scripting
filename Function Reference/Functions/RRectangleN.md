# RRectangleN

## Description
Creates a new rounded rectangle object with the specified bounds

```pascal
PROCEDURE RRectangleN(
				orginX,orginY         : REAL;
				directionX,directionY : REAL;
				width                 : REAL;
				height                : REAL;
				xDiam                 : REAL;
				yDiam                 : REAL);
```

```python
def vs.RRectangleN(orgin, direction, width, height, xDiam, yDiam):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|orgin|REAL|   |
|direction|REAL|   |
|width|REAL|   |
|height|REAL|   |
|xDiam|REAL|   |
|yDiam|REAL|   |

## Examples
```pascal
	EndPoly;
	END;
3:	BEGIN
		Rad := SizeFactor * 0.45;
		RRectangleN( 0, -SizeFactor/2, 1, 0, bubble_width, SizeFactor, Rad, Rad )
	END;
4:	BEGIN
		RectangleN( 0, -SizeFactor/2, 1, 0, bubble_width, SizeFactor )
	END;

BEGIN
	IF ValidNumStr (GetRfield(ghParm, kPIOName,'__TextBubRRRad'),RRCornerRad) THEN BEGIN END;
	RRectangleN (TextX1+BubXShift,TextY2+BubYShift, 90, 0, TextWidth+TextMargin*2, TextHeight+TextMargin*2,RRCornerRad*2,RRCornerRad*2);
END;

	RRectangleN (TextX1+BubXShift,TextY2+BubYShift, 90, 0, TextWidth+TextMargin*2, TextHeight+TextMargin*2,RRCornerRad*2,RRCornerRad*2);
END;
```
```python
import vs

# Creates a new rounded rectangle object with the specified bounds.
orgin = 'Example'
direction = 'C:/Temp'
width = 2.0
height = 2.0
xDiam = 1.0
yDiam = 2.0

vs.RRectangleN(orgin, direction, width, height, xDiam, yDiam)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
