# Space_Set3DGrossHeightOffset

## Description
Set the gross offset height of 3D space object.

```pascal
PROCEDURE Space_Set3DGrossHeightOffset(
				space  : HANDLE;
				offset : REAL;
				selObj : BOOLEAN);
```

```python
def vs.Space_Set3DGrossHeightOffset(space, offset, selObj):
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
Space_Set3DGrossHeightOffset(space, 1.0, TRUE);
```
```python
import vs

# Set the gross offset height of 3D space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
offset = 0.0
selObj = True

vs.Space_Set3DGrossHeightOffset(space, offset, selObj)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
