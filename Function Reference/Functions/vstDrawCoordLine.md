# vstDrawCoordLine

```pascal
PROCEDURE vstDrawCoordLine(
				pt1X, pt1Y : REAL;
				pt2X, pt2Y : REAL);
```

```python
def vs.vstDrawCoordLine(pt1X, pt1Y, pt2X, pt2Y):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1X, pt1Y|REAL|   |
|pt2X, pt2Y|REAL|   |

## Examples
```pascal
BEGIN
vstDrawCoordLine(ObjLoc[TmpIndex].X+OriginX, ObjLoc[TmpIndex].Y+OriginY,tempX+OriginX, tempY+OriginY);
END;

begin
	If Is3dView then
		vstDrawCoordLine3D(x1, y1 , 0, x2, y2, 0)
	else
		vstDrawCoordLine(x1, y1, x2, y2);
end;
```
```python
import vs

pt1X = 1.0
pt1Y = 2.0
pt2X = 0.5
pt2Y = 3.0

vs.vstDrawCoordLine(pt1X, pt1Y, pt2X, pt2Y)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
