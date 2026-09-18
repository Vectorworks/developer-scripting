# CC_GetEquipmentItem

## Description
Gets the associated equipment item from the given device handle.

```pascal
FUNCTION CC_GetEquipmentItem(hDevice : HANDLE): HANDLE;
```

```python
def vs.CC_GetEquipmentItem(hDevice):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDevice|HANDLE|   |

## Examples
```pascal
resultH := CC_GetEquipmentItem(hDevice);
```
```python
import vs

# Gets the associated equipment item from the given device handle.
hDevice = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CC_GetEquipmentItem(hDevice)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2025

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
