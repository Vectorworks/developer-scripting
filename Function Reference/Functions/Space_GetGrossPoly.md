# Space_GetGrossPoly

## Description
Returns gross poly of given space object

```pascal
FUNCTION Space_GetGrossPoly(space : HANDLE): HANDLE;
```

```python
def vs.Space_GetGrossPoly(space):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultH := Space_GetGrossPoly(space);
```
```python
import vs

# Returns gross poly of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.Space_GetGrossPoly(space)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
