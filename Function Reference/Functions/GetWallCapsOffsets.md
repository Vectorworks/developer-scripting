# GetWallCapsOffsets

## Description
Get the wall's caps' offsets.

```pascal
PROCEDURE GetWallCapsOffsets(
				theWall                 : HANDLE;
				VAR leftCapLeftOffset   : REAL;
				VAR leftCapRightOffset  : REAL;
				VAR rightCapLeftOffset  : REAL;
				VAR rightCapRightOffset : REAL);
```

```python
def vs.GetWallCapsOffsets(theWall):
    return (leftCapLeftOffset, leftCapRightOffset, rightCapLeftOffset, rightCapRightOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|leftCapLeftOffset|REAL|Returns the left offset of the left wall cap.|
|leftCapRightOffset|REAL|Returns the right offset of the left wall cap.|
|rightCapLeftOffset|REAL|Returns the left offset of the right wall cap.|
|rightCapRightOffset|REAL|Returns the right offset of the right wall cap.|

## Remarks
CJG 6-27-06

## Examples
```pascal
GetWallCapsOffsets(theWall, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Get the wall's caps' offsets.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer

leftCapLeftOffset, leftCapRightOffset, rightCapLeftOffset, rightCapRightOffset = vs.GetWallCapsOffsets(theWall)
vs.Message('GetWallCapsOffsets returned: ' + str((leftCapLeftOffset, leftCapRightOffset, rightCapLeftOffset, rightCapRightOffset)))
```

## See Also
VS Functions:
[SetWallCapsOffsets](SetWallCapsOffsets.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
