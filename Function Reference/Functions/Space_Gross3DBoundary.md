# Space_Gross3DBoundary

## Description
Returns gross 3D boundary of given space object

```pascal
FUNCTION Space_Gross3DBoundary(space : HANDLE): HANDLE;
```

```python
def vs.Space_Gross3DBoundary(space):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultH := Space_Gross3DBoundary(space);
```
```python
import vs

# Returns gross 3D boundary of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.Space_Gross3DBoundary(space)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
