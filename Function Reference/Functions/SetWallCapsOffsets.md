# SetWallCapsOffsets

## Description
Set the wall's caps' offsets.

```pascal
FUNCTION SetWallCapsOffsets(
				theWall               : HANDLE;
				leftCapLeftDistance   : REAL;
				leftCapRightDistance  : REAL;
				rightCapLeftDistance  : REAL;
				rightCapRightDistance : REAL): BOOLEAN;
```

```python
def vs.SetWallCapsOffsets(theWall, leftCapLeftDistance, leftCapRightDistance, rightCapLeftDistance, rightCapRightDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|leftCapLeftDistance|REAL|The left offset of the left wall cap.|
|leftCapRightDistance|REAL|The right offset of the left wall cap.|
|rightCapLeftDistance|REAL|The left offset of the right wall cap.|
|rightCapRightDistance|REAL|The right offset of the right wall cap.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[GetWallCapsOffsets](GetWallCapsOffsets.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
