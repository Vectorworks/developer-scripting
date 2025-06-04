# GetWallCaps

## Description
Gets the wall's caps.

```pascal
PROCEDURE GetWallCaps(
				theWall      : HANDLE;
				VAR leftCap  : BOOLEAN;
				VAR rightCap : BOOLEAN;
				VAR round    : BOOLEAN);
```

```python
def vs.GetWallCaps(theWall):
    return (leftCap, rightCap, round)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|leftCap|BOOLEAN|Returns whether or not the wall has a left cap.|
|rightCap|BOOLEAN|Returns whether or not the wall has a right cap.|
|round|BOOLEAN|Returns whether or not the wall's caps are round.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[SetWallCaps](SetWallCaps.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
