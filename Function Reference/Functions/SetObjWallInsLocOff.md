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

## See Also
VS Functions:
[GetObjWallInsLocOff](GetObjWallInsLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
