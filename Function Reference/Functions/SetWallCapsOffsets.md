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

## Examples
```pascal
resultOK := SetWallCapsOffsets(theWall, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Set the wall's caps' offsets.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer
leftCapLeftDistance = 1.0
leftCapRightDistance = 1.0
rightCapLeftDistance = 1.0
rightCapRightDistance = 1.0

ok = vs.SetWallCapsOffsets(theWall, leftCapLeftDistance, leftCapRightDistance, rightCapLeftDistance, rightCapRightDistance)
if ok:
    vs.Message('SetWallCapsOffsets succeeded')
else:
    vs.Message('SetWallCapsOffsets failed')
```

## See Also
VS Functions:
[GetWallCapsOffsets](GetWallCapsOffsets.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
