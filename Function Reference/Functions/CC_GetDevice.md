# CC_GetDevice

## Description
Gets the parent device handle from the given socket handle.

```pascal
FUNCTION CC_GetDevice(
				hSocket       : HANDLE;
				skip adapters : BOOLEAN): HANDLE;
```

```python
def vs.CC_GetDevice(hSocket, skip adapters):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSocket|HANDLE|   |
|skip adapters|BOOLEAN|   |

## Examples
```pascal
resultH := CC_GetDevice(hSocket, TRUE);
```
```python
import vs

# Gets the parent device handle from the given socket handle.
hSocket = vs.FSActLayer()  # handle to the first selected object on the active layer
skip adapters = True

objHandle = vs.CC_GetDevice(hSocket, skip adapters)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2025

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
