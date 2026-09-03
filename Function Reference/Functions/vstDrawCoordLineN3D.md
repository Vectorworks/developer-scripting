# vstDrawCoordLineN3D

```pascal
PROCEDURE vstDrawCoordLineN3D(
				pt1X, pt1Y : REAL;
				pt2X, pt2Y : REAL;
				planeRefID : LONGINT);
```

```python
def vs.vstDrawCoordLineN3D(pt1X, pt1Y, pt2X, pt2Y, planeRefID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt1X, pt1Y|REAL|   |
|pt2X, pt2Y|REAL|   |
|planeRefID|LONGINT|   |

## Examples
```pascal
vstDrawCoordLineN3D(1.0, 2.0, 0.5, 1.5, 1);
```
```python
import vs

pt1X = 1.0
pt1Y = 2.0
pt2X = 0.5
pt2Y = 3.0
planeRefID = 1

vs.vstDrawCoordLineN3D(pt1X, pt1Y, pt2X, pt2Y, planeRefID)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
