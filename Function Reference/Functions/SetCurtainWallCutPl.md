# SetCurtainWallCutPl

## Description
Sets the curtain wall cut plane of the wall.

```pascal
PROCEDURE SetCurtainWallCutPl(
				wall                : HANDLE;
				curtainWallCutPlane : REAL);
```

```python
def vs.SetCurtainWallCutPl(wall, curtainWallCutPlane):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|
|curtainWallCutPlane|REAL|The curtain wall cut plane of the wall.|

## Examples
```pascal
SetCurtainWallCutPl(wall, 1.0);
```
```python
import vs

# Sets the curtain wall cut plane of the wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer
curtainWallCutPlane = 1.0

vs.SetCurtainWallCutPl(wall, curtainWallCutPlane)
```

## See Also
VS Functions:
GetCurtainWallCutPlane

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
