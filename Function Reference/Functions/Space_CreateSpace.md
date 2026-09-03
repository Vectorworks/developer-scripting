# Space_CreateSpace

## Description
Creates a new space with the passed polygon

```pascal
FUNCTION Space_CreateSpace(
				space       : HANDLE;
				spaceHeight : REAL): HANDLE;
```

```python
def vs.Space_CreateSpace(space, spaceHeight):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|spaceHeight|REAL|   |

## Examples
```pascal
h := Space_CreateSpace(path, 0);
```
```python
import vs

# Creates a new space with the passed polygon.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
spaceHeight = 2.0

objHandle = vs.Space_CreateSpace(space, spaceHeight)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
