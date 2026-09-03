# RectangleN

## Description
Creates a new rectangle object with the specified bounds.

```pascal
PROCEDURE RectangleN(
				orginX,orginY         : REAL;
				directionX,directionY : REAL;
				width                 : REAL;
				height                : REAL);
```

```python
def vs.RectangleN(orgin, direction, width, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|orgin|REAL|   |
|direction|REAL|   |
|width|REAL|   |
|height|REAL|   |

## Remarks
This procedure does not return a handle.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
RectangleN(0, 0, 1, 0, 1, 1);
END;
RUN(Example);
```
#### Python ####
```python
origin = [0, 1]
direction = [10, 10]
width = 5
height = 2

vs.RectangleN ( origin[0], origin[1], direction[0], direction[1], width, height )
```

```pascal
			Rad := SizeFactor * 0.45;
			RRectangleN( 0, -SizeFactor/2, 1, 0, bubble_width, SizeFactor, Rad, Rad )
		END;
	4:	BEGIN
			RectangleN( 0, -SizeFactor/2, 1, 0, bubble_width, SizeFactor )
		END;
	END; {of CASE}
hBubble := LNewObj;
return := SetTextAdorner(title_h,hBubble,SizeFactor/2,0);
END;

BEGIN
	RectangleN( x1, y1, 1, 0, ( x2 - x1 ), ( y2 - y1 ) );
END;

pioPhotoRsrcPixelW := GetObjectVariableLongint( pioPhotoObjHand, 530 );
pioPhotoRsrcPixelH := GetObjectVariableLongint( pioPhotoObjHand, 531 );
{ instead of keeping a bitmap of the inage, delete it and create a similar size rectangle as a place holder }
DelObjectClearHandProc( pioPhotoObjHand );
RectangleN( -pioPhotoRsrcWidth / 2, -pioPhotoRsrcHeight / 2, 1, 0, pioPhotoRsrcWidth, pioPhotoRsrcHeight );
pioPhotoObjHand := LNewObj;
```
```python
import vs

# Creates a new rectangle object with the specified bounds.
orgin = 'Example'
direction = 'C:/Temp'
width = 2.0
height = 2.0

vs.RectangleN(orgin, direction, width, height)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
