# SetWallThickness

## Description
Sets the thickness of an unstyled wall without components. Will return false for a styled wall or a wall with components. To change the thickness of a wall with components, add, remove or resize components with InsertNewComponent, DeleteComponent, and SetComponent Width

```pascal
FUNCTION SetWallThickness(
				h                 : HANDLE;
				thicknessDistance : REAL): BOOLEAN;
```

```python
def vs.SetWallThickness(h, thicknessDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|thicknessDistance|REAL|   |

## Remarks
NZH 5-10-05

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
