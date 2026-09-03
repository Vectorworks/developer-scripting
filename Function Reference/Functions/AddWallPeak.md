# AddWallPeak

## Description
Procedure AddWallPeak creates a wall peak in the referenced wall object.

```pascal
PROCEDURE AddWallPeak(
				wallHd         : HANDLE;
				offDistance    : REAL;
				heightDistance : REAL);
```

```python
def vs.AddWallPeak(wallHd, offDistance, heightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|offDistance|REAL|Offset distance from wall start.|
|heightDistance|REAL|Elevation of wall peak.|

## Examples
```pascal
AddWallPeak(wallHd, 1.0, 2.0);
```
```python
import vs

# Procedure AddWallPeak creates a wall peak in the referenced wall object.
wallHd = vs.FSActLayer()  # handle to the first selected object on the active layer
offDistance = 1.0
heightDistance = 2.0

vs.AddWallPeak(wallHd, offDistance, heightDistance)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
