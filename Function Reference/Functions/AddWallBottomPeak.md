# AddWallBottomPeak

## Description
Adds a peak to the bottom of the referenced wall.

```pascal
PROCEDURE AddWallBottomPeak(
				wallHd         : HANDLE;
				offDistance    : REAL;
				heightDistance : REAL);
```

```python
def vs.AddWallBottomPeak(wallHd, offDistance, heightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|offDistance|REAL|Offset distance of peak from wall start.|
|heightDistance|REAL|Height of peak.|

## Examples
[CreateWallObject](examples/CreateWallObject.md)

```pascal
AddWallBottomPeak(wallHd, 1.0, 2.0);
```
```python
import vs

# Adds a peak to the bottom of the referenced wall.
wallHd = vs.FSActLayer()  # handle to the first selected object on the active layer
offDistance = 1.0
heightDistance = 2.0

vs.AddWallBottomPeak(wallHd, offDistance, heightDistance)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
