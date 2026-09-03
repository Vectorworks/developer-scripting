# CC_DeviceFromShape

## Description
Creates device from the given shape. The shape must be rectangle, rounded rectangle, polygon or polyline.

```pascal
PROCEDURE CC_DeviceFromShape(hObj : HANDLE);
```

```python
def vs.CC_DeviceFromShape(hObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |

## Examples
```pascal
BEGIN
	gPluginObjH := CC_DeviceFromShape(h);
END;	{of MakeDevice}
```
```python
import vs

# Creates device from the given shape.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.CC_DeviceFromShape(hObj)
```

## Version
Availability: from Vectorworks 2022

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
