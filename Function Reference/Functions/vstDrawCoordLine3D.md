# vstDrawCoordLine3D

```pascal
PROCEDURE vstDrawCoordLine3D(
				pt1 : REAL;
				pt2 : REAL);
```

```python
def vs.vstDrawCoordLine3D(pt1, pt2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1|REAL|   |
|pt2|REAL|   |

## Examples
```pascal
begin
	vstDrawCoordLine3D(ObjLoc[TmpIndex].X+OriginX, ObjLoc[TmpIndex].Y+OriginY,0,tempX+OriginX, tempY+OriginY,0);
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

pt1 = 1.0
pt2 = 2.0

vs.vstDrawCoordLine3D(pt1, pt2)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
