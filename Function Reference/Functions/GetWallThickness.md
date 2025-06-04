# GetWallThickness

## Description
Gets the thickness of a wall

```pascal
FUNCTION GetWallThickness(
				h                 : HANDLE;
				VAR thicknessDist : REAL): BOOLEAN;
```

```python
def vs.GetWallThickness(h):
    return (BOOLEAN, thicknessDist)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|thicknessDist|REAL|   |

## Remarks
Same functionality as WallWidth(h), except that GetWallThickness returns also a Boolean, which may help in program flow branching.

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
