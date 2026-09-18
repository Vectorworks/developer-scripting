# MoveWallByOffset

## Description
Available in Architect only. Moves the wall perpendicular to its definition line by the specified offset and maintains all wall connections. Wall movement may be constrained by the surrounding geometry so the actual amount of the offset is returned.

```pascal
PROCEDURE MoveWallByOffset(
				theWall    : HANDLE;
				VAR offset : REAL);
```

```python
def vs.MoveWallByOffset(theWall, offset):
    return offset
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|A handle to the wall to move.|
|offset|REAL|The distance to move the given wall. Negative offsets move the wall to the left and positive offsets move the wall to the right. The actual amount the wall was moved is returned in this field.|

## Examples
```pascal
MoveWallByOffset(theWall, 1.0);
```
```python
import vs

# Available in Architect only.
theWall = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0

result = vs.MoveWallByOffset(theWall, offset)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
