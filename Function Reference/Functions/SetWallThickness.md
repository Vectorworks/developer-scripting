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

## Examples
```pascal
resultOK := SetWallThickness(h, 1.0);
```
```python
import vs

# Sets the thickness of an unstyled wall without components.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
thicknessDistance = 0.1

ok = vs.SetWallThickness(h, thicknessDistance)
if ok:
    vs.Message('SetWallThickness succeeded')
else:
    vs.Message('SetWallThickness failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
