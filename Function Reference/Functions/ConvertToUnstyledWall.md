# ConvertToUnstyledWall

## Description
Sets a wall to be unstyled.

```pascal
FUNCTION ConvertToUnstyledWall(h : HANDLE): BOOLEAN;
```

```python
def vs.ConvertToUnstyledWall(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Remarks
Sets a wall to be unstyled. This allows a wall to then be manipulated by certain functions that will not work on a styled wall.

## Examples
```pascal
resultOK := ConvertToUnstyledWall(h);
```
```python
import vs

# Sets a wall to be unstyled.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.ConvertToUnstyledWall(h)
if ok:
    vs.Message('ConvertToUnstyledWall succeeded')
else:
    vs.Message('ConvertToUnstyledWall failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
