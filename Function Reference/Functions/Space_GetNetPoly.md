# Space_GetNetPoly

## Description
Returns net poly of given space object

```pascal
FUNCTION Space_GetNetPoly(space : HANDLE): HANDLE;
```

```python
def vs.Space_GetNetPoly(space):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultH := Space_GetNetPoly(space);
```
```python
import vs

# Returns net poly of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.Space_GetNetPoly(space)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
