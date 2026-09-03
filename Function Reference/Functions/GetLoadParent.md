# GetLoadParent

## Description
Get the count of cells attached to a Lighting Device.

```pascal
FUNCTION GetLoadParent(handle : HANDLE): HANDLE;
```

```python
def vs.GetLoadParent(handle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |

## Examples
```pascal
resultH := GetLoadParent(handle);
```
```python
import vs

# Get the count of cells attached to a Lighting Device.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetLoadParent(handle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2025

## Category
* [Spotlight](../Categories/Spotlight.md)
