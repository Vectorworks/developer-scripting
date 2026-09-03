# SetObjectWallHeight

## Description
Sets an object's height value in it's break record.

The object (objH) must be contained in wall (wallH)  to succeed.

```pascal
FUNCTION SetObjectWallHeight(
				objH   : HANDLE;
				wallH  : HANDLE;
				height : REAL (Coordinate)): BOOLEAN;
```

```python
def vs.SetObjectWallHeight(objH, wallH, height):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|height|REAL (Coordinate)|   |

## Examples
```pascal
SetObjectWallHeight(objH, wallH, 1.0);
```
```python
import vs

# Sets an object's height value in it's break record.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
height = 2.0

ok = vs.SetObjectWallHeight(objH, wallH, height)
if ok:
    vs.Message('SetObjectWallHeight succeeded')
else:
    vs.Message('SetObjectWallHeight failed')
```

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
