# Space_Set3DNetHeightOffset

## Description
Set the net offset height of 3D space object.

```pascal
PROCEDURE Space_Set3DNetHeightOffset(
				space  : HANDLE;
				offset : REAL;
				selObj : BOOLEAN);
```

```python
def vs.Space_Set3DNetHeightOffset(space, offset, selObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|offset|REAL|   |
|selObj|BOOLEAN|   |

## Examples
```pascal
Space_Set3DNetHeightOffset(space, 1.0, TRUE);
```
```python
import vs

# Set the net offset height of 3D space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0
selObj = True

vs.Space_Set3DNetHeightOffset(space, offset, selObj)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
