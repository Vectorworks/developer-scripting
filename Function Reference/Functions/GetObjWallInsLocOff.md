# GetObjWallInsLocOff

## Description
Gets the insert location offset of an object in a wall.

```pascal
FUNCTION GetObjWallInsLocOff(
				objectHandle             : HANDLE;
				wallHandle               : HANDLE;
				VAR insertLocationOffset : REAL): BOOLEAN;
```

```python
def vs.GetObjWallInsLocOff(objectHandle, wallHandle):
    return (BOOLEAN, insertLocationOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object in the wall.|
|wallHandle|HANDLE|The wall.|
|insertLocationOffset|REAL|Returns the insert location offset.|

## See Also
VS Functions:
[SetObjWallInsLocOff](SetObjWallInsLocOff.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
