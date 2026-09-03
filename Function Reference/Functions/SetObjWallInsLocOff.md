# SetObjWallInsLocOff

## Description
Sets the insert location offset for an object in a wall.

```pascal
FUNCTION SetObjWallInsLocOff(
				objectHandle         : HANDLE;
				wallHandle           : HANDLE;
				insertLocationOffset : REAL (Coordinate)): BOOLEAN;
```

```python
def vs.SetObjWallInsLocOff(objectHandle, wallHandle, insertLocationOffset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object in the wall.|
|wallHandle|HANDLE|The wall.|
|insertLocationOffset|REAL (Coordinate)|The insert location offset.|

## Examples
```pascal
SetObjWallInsLocOff(objectHandle, wallHandle, 1.0);
```
```python
import vs

# Sets the insert location offset for an object in a wall.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
wallHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
insertLocationOffset = 0.0

ok = vs.SetObjWallInsLocOff(objectHandle, wallHandle, insertLocationOffset)
if ok:
    vs.Message('SetObjWallInsLocOff succeeded')
else:
    vs.Message('SetObjWallInsLocOff failed')
```

## See Also
VS Functions:
[GetObjWallInsLocOff](GetObjWallInsLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
